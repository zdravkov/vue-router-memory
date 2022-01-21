<template>
<div>
  <div role="grid" >
     <div role="presentation"
      style="padding: 0px;"><div role="presentation">
        <table role="presentation"><colgroup role="presentation">
        <col></colgroup>
        <thead role="presentation" data-keyboardnavheader="true" >
          <tr>
            <th aria-sort="none" colspan="1" rowspan="1" role="columnheader"
           >ProductID</th></tr>
             </thead>
        </table>
      </div>
    </div>
             <div role="presentation" >
               <div role="presentation" >
                 <div style="position: relative;">
                   <table role="presentation" tabindex="-1" >
                     <colgroup role="presentation"><col></colgroup>
                     <tbody role="presentation" >
                       <trcomponent v-for="item in result"
                       :value="item.ProductID" :key="item.ProductID" />
                     </tbody>
                   </table>
                   </div>
                   </div>
             </div>
    </div> 
</div>
</template>
<script>
import trComponent from './trComponent'

export default {
    components: {
      trcomponent: trComponent
    },
    beforeDestroy(){
    },
    data: function () {
        return {
            columns: [
                { field: 'ProductID'},
            ],
             result:this.createRandomData(10000)
        };
    },
    methods: {
        sortChangeHandler: function(e) {
            this.sort = e.sort;
        },
        createRandomData(count) {


            return Array(count).fill({}).map((_, idx) => ({
                ProductID: idx + 1,
 
            }));
        }
    }
};

</script>