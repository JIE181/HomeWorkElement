<template>
    <div>
      <el-card class="box-card">
        <template v-slot:header>
          <h3>电商销售数据</h3>
        </template>
        <el-table :data="salesData" style="width: 100%">
          <el-table-column prop="product" label="产品"></el-table-column>
          <el-table-column prop="sales" label="销售额"></el-table-column>
          <el-table-column label="操作">
            <template v-slot:default="scope">
              <el-button @click="modifySales(scope.row)">修改数量</el-button>
            </template>
          </el-table-column>
        </el-table>
      </el-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        salesData: [
          { product: '产品A', sales: 5000 },
          { product: '产品B', sales: 8000 },
          { product: '产品C', sales: 3000 }
        ]
      }
    },
    methods: {
      modifySales(row) {
        const newSales = prompt(`请输入${row.product}的新销售额`, row.sales)
        if (newSales !== null) {
          row.sales = parseInt(newSales)
        }
      }
    }
  }
  </script>
  
  <style scoped>
  .box-card {
    margin-bottom: 20px;
  }
  </style>