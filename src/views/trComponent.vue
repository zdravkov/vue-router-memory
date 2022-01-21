<template>
  <tr
        role="row" 
        aria-rowindex="2" 
    data-grid-row-index="-1" 
    class="k-master-row">
    <td colspan="1" role="gridcell" data-grid-col-index="0">
        {{value + "Item"}}
    </td>
     </tr>
</template>
<script>

export default {
   props: {
       value: Number
   }
};

</script>