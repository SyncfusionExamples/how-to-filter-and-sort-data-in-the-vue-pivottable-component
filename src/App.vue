<script>
  import { PivotViewComponent, GroupingBar } from "@syncfusion/ej2-vue-pivotview";
  
export default{
  components: {
    "ejs-pivotview": PivotViewComponent
  },
  data()
  {
    return{
      dataSourceSettings:{
        dataSource:[
            { Units: "Business-1", Amount: 5100, Country: "Canada", Date: "FY 2006", Product: "Car", Quantity: 21, State: "Alberta" },
            { Units: "Business-21", Amount: 1900, Country: "France", Date: "FY 2007", Product: "Bike", Quantity: 23, State: "Alberta" },
            { Units: "Business-32", Amount: 1000, Country: "Sweden", Date: "FY 2008", Product: "Car", Quantity: 29, State: "Alberta" },
            { Units: "Business-43", Amount: 2060, Country: "Canada", Date: "FY 2006", Product: "Bike", Quantity: 93, State: "British Columbia" },
            { Units: "Business-2", Amount: 6200, Country: "France", Date: "FY 2007", Product: "Car", Quantity: 36, State: "British Columbia" },
            { Units: "Business-15", Amount: 2000, Country: "Sweden", Date: "FY 2008", Product: "Bike", Quantity: 31, State: "British Columbia" },
            { Units: "Business-67", Amount: 1300, Country: "Canada", Date: "FY 2005", Product: "Car", Quantity: 45, State: "Brunswick" },
            { Units: "Business-12", Amount: 3400, Country: "France", Date: "FY 2006", Product: "Bike", Quantity: 47, State: "Brunswick" },
            { Units: "Business-10", Amount: 2300, Country: "Sweden", Date: "FY 2007", Product: "Car", Quantity: 43, State: "Brunswick" },
            { Units: "Business-11", Amount: 5150, Country: "Canada", Date: "FY 2006", Product: "Bike", Quantity: 21, State: "Alberta" },
            { Units: "Business-31", Amount: 1970, Country: "France", Date: "FY 2007", Product: "Car", Quantity: 23, State: "Alberta" },
            { Units: "Business-13", Amount: 1030, Country: "Sweden", Date: "FY 2008", Product: "Bike", Quantity: 29, State: "Alberta" },
            { Units: "Business-41", Amount: 2000, Country: "Canada", Date: "FY 2006", Product: "Car", Quantity: 93, State: "British Columbia" },
            { Units: "Business-56", Amount: 6250, Country: "France", Date: "FY 2007", Product: "Bike", Quantity: 36, State: "British Columbia" },
            { Units: "Business-61", Amount: 2020, Country: "Sweden", Date: "FY 2008", Product: "Car", Quantity: 31, State: "British Columbia" },
            { Units: "Business-19", Amount: 1390, Country: "Canada", Date: "FY 2005", Product: "Bike", Quantity: 45, State: "Brunswick" },
            { Units: "Business-22", Amount: 3460, Country: "France", Date: "FY 2006", Product: "Car", Quantity: 47, State: "Brunswick" },
            { Units: "Business-18", Amount: 2380, Country: "Sweden", Date: "FY 2007", Product: "Bike", Quantity: 43, State: "Brunswick" },
        ],
        rows: [{name:'Units', dataType:'Number'}],
        columns: [{name:'Date'}],
        values: [{name:'Amount'}, {name:'Quantity'}],
        formatSettings: [{name:'Amount', format:'C1'}],
        filterSettings: [{name:'Quantity', type:'Number', condition:'Between', value1:30, value2:40}],
        allowLabelFilter: true,
        allowValueFilter: true,
        valueSortSettings: {
            headerText: 'FY 2006##Amount',
            headerDelimiter: '##',
            sortOrder: 'Descending'
        },
      },
      
      height:'350px',
      width:'900px',
      showGroupingBar: true,
      maxNodeLimitInMemberEditor:2,
      enableValueSorting: true
    };
  } ,
  provide:
  {
    pivotview:[GroupingBar]
  }
}
</script>

<template>
  <ejs-pivotview :height="height" :width="width"
                :dataSourceSettings="dataSourceSettings"
                :showGroupingBar ="showGroupingBar"
                :maxNodeLimitInMemberEditor="maxNodeLimitInMemberEditor"
                :enableValueSorting="enableValueSorting"></ejs-pivotview>
</template>

<style >
  @import "../node_modules/@syncfusion/ej2-base/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-inputs/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-buttons/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-splitbuttons/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-calendars/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-dropdowns/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-lists/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-popups/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-navigations/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-grids/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-vue-pivotview/styles/bootstrap5.css";
 </style>


