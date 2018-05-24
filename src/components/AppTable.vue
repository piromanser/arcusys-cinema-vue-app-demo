<template>
  <table align="center" border="1" style="cursor: pointer; border: none;" @click="onTableClick">

        <tr>

            <td>

                <div class="chair">R1C1</div>

            </td>

            <td>

                <div class="chair">R1C2</div>

            </td>

            <td>

                <div class="chair">R1C3</div>

            </td>

            <td>

                <div class="chair">R1C4</div>

            </td>

        </tr>

        <tr>

            <td>

                <div class="chair">R2C1</div>

            </td>

            <td>

                <div class="chair">R2C2</div>

            </td>

            <td>

                <div class="chair">R2C3</div>

            </td>

            <td>

                <div class="chair">R2C4</div>

            </td>

        </tr>

        <tr>

            <td>

                <div class="chair">R3C1</div>

            </td>

            <td>

                <div class="chair">R3C2</div>

            </td>

            <td>

                <div class="chair">R3C3</div>

            </td>

            <td>

                <div class="chair">R3C4</div>

            </td>

        </tr>

        <tr>

            <td>

                <div class="chair">R4C1</div>

            </td>

            <td>

                <div class="chair">R4C2</div>

            </td>

            <td>

                <div class="chair">R4C3</div>

            </td>

            <td>

                <div class="chair">R4C4</div>

            </td>

        </tr>

    </table>
</template>


<script>
export default {
  methods: {
    onTableClick(event) {
      const cel = event.target
      if (cel.tagName !== 'DIV') {
        return
      }
      const reserve =  confirm('Would you like to reserve that place?');
      if (reserve) {
        cel.classList.add('chair-reserved')
      }
      
      
    }
  },
}
</script>


<style>

.chair { 
    width: 32px;
    height: 32px;
    background-image: url('../assets/free-chair.png');
}
.chair-reserved {
    background-image: url('../assets/reserved-chair.png');
}
td {
    border: none;
}


</style>
