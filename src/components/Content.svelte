<script>
import { alimentos} from './alimentos.js';

var sel=null;
function updateSelectedCategory(e) {
    selectedCategory = e.target.TextContent;
  }

</script>
{#each alimentos as alimento,i }

<button on:clikc={(sel) => sel = this.value}>{alimento.alimento}</button>

{/each}

{#if sel!=null}

<p>{alimentos[sel].explicacion}</p>
{/if}


<style>

main{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  gap: 20px;

}
.contenedor {
  border-radius:10px;
  text-align:center;
  border: 1px solid black;
  display:inline-block;
  flex-wrap:wrap;
  gap:20px;
  transition:ease-in-out

}

.alimento {
  font-weight: bold;
}
</style>


