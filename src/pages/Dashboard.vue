<template>
  <div class="content">
    <div class="md-layout">
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <h3 style="color: #495057 !important">World Wide</h3>
      </div>
    </div>
    <div class="md-layout">
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="dark">
          <template slot="header">
            <md-icon>group</md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Cases</p>
            <h4 class="title">{{ cases }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="purple">
          <template slot="header">
            <md-icon>people_alt</md-icon>
          </template>

          <template slot="content">
            <p class="category">New Cases</p>
            <h4 class="title">{{ todayCases }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="blue">
          <template slot="header">
            <md-icon>hotel</md-icon>
          </template>

          <template slot="content">
            <p class="category">Active Cases</p>
            <h4 class="title">{{ active }}</h4>
          </template>
        </stats-card>
      </div>

      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="orange">
          <template slot="header">
            <md-icon>hotel</md-icon>
          </template>

          <template slot="content">
            <p class="category">Critical Cases</p>
            <h4 class="title">{{ critical }}</h4>
          </template>
        </stats-card>
      </div>

      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="green">
          <template slot="header">
            <md-icon>how_to_reg</md-icon>
          </template>

          <template slot="content">
            <p class="category">Recovered</p>
            <h4 class="title">{{ recovered }}</h4>
          </template>

          <!-- <template slot="footer">
            <div class="stats">
              <md-icon>local_offer</md-icon>
              Tracked from Github
            </div>
          </template>-->
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon>mood_bad</md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Deaths</p>
            <h4 class="title">{{ deaths }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon>mood_bad</md-icon>
          </template>

          <template slot="content">
            <p class="category">Today's Deaths</p>
            <h4 class="title">{{ todayDeaths }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="red">
          <template slot="header">
            <i class="fas fa-user"></i>
          </template>

          <template slot="content">
            <p class="category">Total Test</p>
            <h4 class="title" style="font-size: 20px;">{{ tests }}</h4>
          </template>
        </stats-card>
      </div>
      <!-- end global info -->

      <div class="md-layout mt-5">
        <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
          <h3 style="color: #495057 !important">Bangladesh</h3>
        </div>
      </div>

      <div class="md-layout-item md-size-100">
        <iframe
          src="https://corona.in.com.bd/widget2"
          height="205"
          width="100%"
          frameborder="0"
          style="height: 205px;"
        ></iframe>
      </div>
      <div class="md-layout-item md-size-50 sm-size-100 mt-4">
        <iframe
          src="https://corona.in.com.bd/widget1"
          height="300"
          width="300"
          frameborder="0"
          style="width: 100%;height: 320px;"
        ></iframe>
      </div>
      <div class="md-layout-item md-size-50 sm-size-100 mt-4">
        <iframe
          src="https://corona.in.com.bd/widget3"
          height="300"
          width="300"
          frameborder="0"
          style="width: 100%; height: 320px;"
        ></iframe>
      </div>




      <!-- bd stats -->
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="orange">
          <template slot="header">
            <md-icon>hotel</md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Confirmed</p>
            <h4 class="title">{{ totalConfirmedBd }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="green">
          <template slot="header">
            <md-icon>how_to_reg</md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Recovered</p>
            <h4 class="title">{{ totalRecoveredBd }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon>mood_bad</md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Deaths</p>
            <h4 class="title">{{ totalDeathsBd }}</h4>
          </template>
        </stats-card>
      </div>

      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="purple">
          <template slot="header">
            <i class="fas fa-user"></i>
          </template>

          <template slot="content">
            <p class="category">Total Tested</p>
            <h4 class="title">{{ totalTestedBd }}</h4>
          </template>
        </stats-card>
      </div>

      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="orange">
          <template slot="header">
            <md-icon>hotel</md-icon>
          </template>

          <template slot="content">
            <p class="category">New Confirmed</p>
            <h4 class="title">{{ lastConfirmedBd }}</h4>
          </template>

          <!-- <template slot="footer">
            <div class="stats">
              <md-icon>local_offer</md-icon>
              Tracked from Github
            </div>
          </template>-->
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="green">
          <template slot="header">
            <md-icon>how_to_reg</md-icon>
          </template>

          <template slot="content">
            <p class="category">New Recovered</p>
            <h4 class="title">{{ lastRecoveredBd }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon>mood_bad</md-icon>
          </template>

          <template slot="content">
            <p class="category">New Deaths</p>
            <h4 class="title">{{ lastDeathsBd }}</h4>
          </template>
        </stats-card>
      </div>
      <div class="md-layout-item md-medium-size-50 md-xsmall-size-50 md-size-25">
        <stats-card data-background-color="purple">
          <template slot="header">
            <i class="fas fa-user"></i>
          </template>

          <template slot="content">
            <p class="category">New Tested</p>
            <h4 class="title">{{ lastTestedBd }}</h4>
          </template>
        </stats-card>
      </div>




      <!-- Total Statistic of Bangladesh -->
      <div class="md-layout-item md-size-100 mt-4">
        <b-card title="Total Statistic of Bangladesh">
          <line-chart
            :legend="true"
            xtitle="Date"
            ytitle="Count"
            :data="lineChartDays"
            style="height: 450px;"
          ></line-chart>
        </b-card>
      </div>

      <!-- Gender Ratio (Confirmed) -->
      <div class="md-layout-item md-size-50 mt-4">
        <b-card title="Gender Ratio (Confirmed)">
          <pie-chart suffix="%" :data="pieGenderConfirmed"></pie-chart>
        </b-card>
      </div>

      <!-- Gender Ratio (Deaths) -->
      <div class="md-layout-item md-size-50 mt-4">
        <b-card title="Gender Ratio (Deaths)">
          <pie-chart suffix="%" :data="pieGenderDeaths"></pie-chart>
        </b-card>
      </div>

      <!-- Age Wise Confirmed -->
      <div class="md-layout-item md-size-100 mt-4">
        <b-card title="Age Wise Confirmed">
          <column-chart
            xtitle="Age Range"
            ytitle="Confirmed"
            suffix="%"
            :data="barAgeConfirm"
            style="height: 450px;"
          ></column-chart>
        </b-card>
      </div>

      <!-- Districts wise Datatable  -->
      <div class="md-layout-item md-size-100 mt-4">
        <b-card title="Districts wise data">
          <v-client-table :data="tableData" :columns="columns" :options="options" />
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
import { StatsCard, ChartCard } from "@/components";
import axios from "axios";
import moment from "moment";
import { ServerTable, ClientTable, Event } from "vue-tables-2";

export default {
  components: {
    StatsCard
  },
  data() {
    return {
      // world wise
      cases: "",
      todayCases: "",
      deaths: "",
      todayDeaths: "",
      recovered: "",
      active: "",
      critical: "",
      tests: "",

      // bd data
      totalConfirmedBd: "",
      totalRecoveredBd: "",
      totalDeathsBd: "",
      totalTestedBd: "",

      lastConfirmedBd: "",
      lastRecoveredBd: "",
      lastDeathsBd: "",
      lastTestedBd: "",

      loading: false,
      lineChartDays: {},
      pieGenderConfirmed: [],
      pieGenderDeaths: [],
      barAgeConfirm: [],
      columns: ["City", "Confirmed", "Recovered", "Deaths"],
      tableData: [],
      options: {
        // see the options API
        theme: "bootstrap4"
      }
    };
  },
  mounted() {
    // this.getAllCountriesData();
    this.getGlobalData();
    // this.getAllCountry();
    this.getBdData();
  },
  methods: {
    getGlobalData() {
      axios.get("https://corona.lmao.ninja/v2/all").then(response => {
        this.cases = response.data.cases;
        this.todayCases = response.data.todayCases;
        this.deaths = response.data.deaths;
        this.todayDeaths = response.data.todayDeaths;
        this.recovered = response.data.recovered;
        this.active = response.data.active;
        this.critical = response.data.critical;
        this.tests = response.data.tests;
      });
    },

    getBdData() {
      axios.get("https://corona.in.com.bd/api/stats").then(response => {
        this.totalConfirmedBd = response.data.total.confirmed;
        this.totalRecoveredBd = response.data.total.recovered;
        this.totalDeathsBd = response.data.total.deaths;
        this.totalTestedBd = response.data.total.tested;

        this.lastConfirmedBd = response.data.last.confirmed;
        this.lastRecoveredBd = response.data.last.recovered;
        this.lastDeathsBd = response.data.last.deaths;
        this.lastTestedBd = response.data.last.tested;
      });

      axios.get("https://corona.in.com.bd/api/details").then(response => {
        let apiData = response.data.data.sort(this.custom_sort);
        apiData = apiData.reverse(); // for created_at

        let confirmed = apiData.reduce(function(data, item) {
          // data[moment(item.created_at).format('YYYY-MM-DD')] = item.confirmed;
          data[item.created_at] = item.confirmed;
          return data;
        }, {});

        let recovered = apiData.reduce(function(data, item) {
          data[item.created_at] = item.recovered;
          return data;
        }, {});

        let deaths = apiData.reduce(function(data, item) {
          data[item.created_at] = item.deaths;
          return data;
        }, {});

        var data = [
          { name: "Confirmed", data: confirmed },
          { name: "Deaths", data: deaths },
          { name: "Recovered", data: recovered }
        ];

        this.lineChartDays = data;
      });

      axios.get("https://corona.in.com.bd/api/genders").then(response => {
        this.pieGenderConfirmed = [
          ["Male", response.data.data.male.confirmed],
          ["Female", response.data.data.female.confirmed]
        ];
        this.pieGenderDeaths = [
          ["Male", response.data.data.male.deaths],
          ["Female", response.data.data.female.deaths]
        ];
      });

      axios.get("https://corona.in.com.bd/api/ages").then(response => {
        var ageRange = "";
        this.barAgeConfirm = Object.keys(response.data.data).map(function(
          key,
          value
        ) {
          if (key == "onetoten") {
            ageRange = "1-10";
          }
          if (key == "eleventotwenty") {
            ageRange = "11-20";
          }
          if (key == "twentyonetothirty") {
            ageRange = "21-30";
          }
          if (key == "thirtyonetofourty") {
            ageRange = "31-40";
          }
          if (key == "fourtyonetofifty") {
            ageRange = "41-50";
          }
          if (key == "fiftyonetosixty") {
            ageRange = "51-60";
          }
          if (key == "sixtyplus") {
            ageRange = "60+";
          }
          return [ageRange, response.data.data[key].confirmed];
        });
      });

      axios.get("https://corona.in.com.bd/api/districts").then(response => {
        // table data example
        // tableData: [
        //     { id: 1, name: "John", age: "20" },
        //     { id: 2, name: "Jane", age: "24" },
        //     { id: 3, name: "Susan", age: "16" },
        //     { id: 4, name: "Chris", age: "55" },
        //     { id: 5, name: "Dan", age: "40" }
        // ],

        this.tableData = response.data.data.map(function(item) {
          var city = item.name;
          var confirmed = item.confirmed;
          var recovered = item.recovered;
          var deaths = item.deaths;
          return {
            City: city,
            Confirmed: confirmed,
            Recovered: recovered,
            Deaths: deaths
          };
        });
      });
    },

    custom_sort(a, b) {
      return new Date(b.created_at) - new Date(a.created_at);
    }
  }
};
</script>
