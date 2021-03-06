<template>
  <table class="table table-striped">
    <thead>
    <tr v-for="(row,i) in headColumnsData" :key="i">
      <td v-for="cell in row" :colspan="cell.width" :rowspan="cell.height" :key="cell.id">{{ cell.name }}</td>
    </tr>
    </thead>
    <tbody>
    <tr>
      <td>Lorem ipsum dolor sit amet.</td>
      <td>Culpa id ipsa quod veritatis?</td>
      <td>Doloremque magni perferendis qui sequi.</td>
      <td>Culpa laborum nesciunt quisquam sint.</td>
      <td>Animi non qui quibusdam voluptatibus!</td>
      <td>Ipsa maxime quas quod recusandae.</td>
      <td>Dolores fuga iusto qui saepe?</td>
      <td>Assumenda deleniti ipsam possimus voluptate.</td>
      <td>Aperiam cum dolorem laudantium praesentium?</td>
    </tr>
    </tbody>
  </table>
</template>

<script>
import columnData from "@/data/data.json"

export default {
  name: "TableRenderer",
  data() {
    return {
      headColumnsData: columnData.head
    }
  }
}
</script>

<style lang="scss">
table {
  text-align: center;
  border-collapse: collapse;
  margin: 10px;
}

thead {
  font-weight: bold;
}

td {
  border: 1px solid lightblue;
}
</style>