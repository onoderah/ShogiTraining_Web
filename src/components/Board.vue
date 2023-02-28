<script lang="ts">
export default {
  data() {
    return {
      positions: {
        xAxesPositions: ['９', '８', '７', '６', '５', '４', '３', '２', '１'],
        yAxesPositions: ['一', '二', '三', '四', '五', '六', '七', '八', '九']
      }
    }
  },
  methods: {
    clickColumn: function (xAxes: string, yAxes: string) {
      alert(`${xAxes}${yAxes}`)
    }
  }
}
</script>

<template>
  <v-data-table class="board">
    <tbody>
      <tr v-for="y in positions.yAxesPositions" :key="y">
        <td v-for="x in positions.xAxesPositions" :key="x" @click="clickColumn(x, y)"></td>
      </tr>
    </tbody>
  </v-data-table>
</template>

<style scoped>
.board {
  /*background-color: #c9a61b;*/
}

.board td {
  padding: 0;
  width: 50px;
  height: 50px;
  border: 1px solid #222;
}

.board td:hover {
  background: #246cbd !important;
  cursor: pointer;
}
</style>
