<template>
  <div id="app">
    <GGanttChart
      :chart-start="tabla1.myChartStart"
      :chart-end="tabla1.myChartEnd"
      grid="false"
      :theme="'dark'"
    >
      <GGanttRow
        v-for="row in tabla1.rows"
        :key="row.label"
        :label="row.label"
        :bars="row.bars"
        bar-start="myStart"
        bar-end="myEnd"
      />
    </GGanttChart>
    <br />
    <table>
      <thead>
        <tr>
          <th>Proceso</th>
          <th>T. Llegada</th>
          <th>Rafaga</th>
          <th>T. Comienzo</th>
          <th>T. Final</th>
          <th>T. Retorno</th>
          <th>T. Espera</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>A<br /></td>
          <td>0</td>
          <td>8</td>
          <td>0</td>
          <td>8</td>
          <td>8</td>
          <td>0</td>
        </tr>
        <tr>
          <td>B</td>
          <td>1</td>
          <td>4</td>
          <td>8</td>
          <td>12</td>
          <td>11</td>
          <td>7</td>
        </tr>
        <tr>
          <td>C</td>
          <td>2</td>
          <td>9</td>
          <td>12</td>
          <td>21</td>
          <td>19</td>
          <td>10</td>
        </tr>
        <tr>
          <td>D</td>
          <td>3</td>
          <td>5</td>
          <td>21</td>
          <td>26</td>
          <td>23</td>
          <td>18</td>
        </tr>
        <tr>
          <td>E</td>
          <td>4</td>
          <td>2</td>
          <td>26</td>
          <td>28</td>
          <td>24</td>
          <td>22</td>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td>17</td>
          <td>11.4</td>
        </tr>
      </tbody>
    </table>
    <GGanttChart
      :chart-start="tabla1.myChartStart"
      :chart-end="tabla1.myChartEnd"
      grid="false"
      :theme="'dark'"
    >
      <GGanttRow
        v-for="row in tabla1.rows"
        :key="row.label"
        :label="row.label"
        :bars="row.bars"
        bar-start="myStart"
        bar-end="myEnd"
      />
    </GGanttChart>
    <br />
    <table>
      <thead>
        <tr>
          <th>Proceso</th>
          <th>T. Llegada</th>
          <th>Rafaga</th>
          <th>T. Comienzo</th>
          <th>T. Final</th>
          <th>T. Retorno</th>
          <th>T. Espera</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>A<br /></td>
          <td>0</td>
          <td>8</td>
          <td>0</td>
          <td>8</td>
          <td>8</td>
          <td>0</td>
        </tr>
        <tr>
          <td>B</td>
          <td>1</td>
          <td>4</td>
          <td>8</td>
          <td>12</td>
          <td>11</td>
          <td>7</td>
        </tr>
        <tr>
          <td>C</td>
          <td>2</td>
          <td>9</td>
          <td>12</td>
          <td>21</td>
          <td>19</td>
          <td>10</td>
        </tr>
        <tr>
          <td>D</td>
          <td>3</td>
          <td>5</td>
          <td>21</td>
          <td>26</td>
          <td>23</td>
          <td>18</td>
        </tr>
        <tr>
          <td>E</td>
          <td>4</td>
          <td>2</td>
          <td>26</td>
          <td>28</td>
          <td>24</td>
          <td>22</td>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td>17</td>
          <td>11.4</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { GGanttChart, GGanttRow } from "vue-ganttastic";

export default {
  name: "App",
  components: {
    GGanttChart,
    GGanttRow,
  },
  data() {
    return {
      tabla1: {
        myChartStart: "2021-09-01 00:00",
        myChartEnd: "2021-09-03 00:00",
        rows: [
          {
            label: "A",
            bars: [
              {
                myStart: "2021-09-01 00:00",
                myEnd: "2021-09-01 09:00",
                label: "A",
                ganttBarConfig: {
                  color: "#000",
                  backgroundColor: "#7F9421",
                  borderRadius: 0,
                },
              },
            ],
          },
          {
            label: "B",
            bars: [
              {
                myStart: "2021-09-01 09:00",
                myEnd: "2021-09-01 13:00",
                label: "¿B",
                ganttBarConfig: {
                  color: "#000",
                  backgroundColor: "#E4FF6B",
                  borderRadius: 0,
                },
              },
            ],
          },
          {
            label: "C",
            bars: [
              {
                myStart: "2021-09-01 13:00",
                myEnd: "2021-09-01 22:00",
                label: "C",
                ganttBarConfig: {
                  color: "#000",
                  backgroundColor: "#C5E048",
                  borderRadius: 0,
                },
              },
            ],
          },
          {
            label: "D",
            bars: [
              {
                myStart: "2021-09-01 22:00",
                myEnd: "2021-09-02 03:00",
                label: "D",
                ganttBarConfig: {
                  color: "white",
                  backgroundColor: "#641294",
                  borderRadius: 0,
                },
              },
            ],
          },
          {
            label: "E",
            bars: [
              {
                myStart: "2021-09-02 03:00",
                myEnd: "2021-09-02 05:00",
                label: "E",
                ganttBarConfig: {
                  color: "#000",
                  backgroundColor: "#A948E0",
                  borderRadius: 0,
                },
              },
            ],
          },
        ],
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
