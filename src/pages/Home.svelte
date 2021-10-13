<script>
    import Hero from "../components/Hero.svelte";
    import {link} from "svelte-routing";
//featured products
import Featured from "../components/Products/Featured.svelte";
/* function getProps(){
    return {class: "btn btn-primary btn-hero"}
} */
</script>


<h1>welcome to home page</h1>

<Hero>
    <a href="/products" class="btn btn-primary btn-hero" use:link>Shop now</a>
</Hero>

<Featured title="Featured Products" />