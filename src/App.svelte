<script>

  import { Route,Router } from "svelte-routing";
  import Navbar from "./components/Navbar/Navbar.svelte";
  import Sidebar from "./components/Navbar/Sidebar.svelte";
  import Cart from "./components/Cart/Cart.svelte";
  import About from "./pages/About.svelte";
  import Checkout from "./pages/Checkout.svelte";
  import Home from "./pages/Home.svelte";
  import Login from "./pages/Login.svelte";
  import Products from "./pages/Products.svelte";
  import ProductTemplate from "./pages/ProductTemplate.svelte";
  import globalStore from "./stores/globalStore";



  console.log(globalStore);
  console.log($globalStore);

</script>

<Router>
  <Navbar />
  {#if $globalStore.sidebar}
    <Sidebar />
  {/if}
  
  {#if $globalStore.cart}
    <Cart />
  {/if}

  <Route path="/" component={Home} />
  <Route path="/about" component={About} />
  <Route path="/login" component={Login} />
  <Route path="/checkout" component={Checkout} />
  <Route path="/products" component={Products} />
  <Route path="/products/:id" component={ProductTemplate} />
</Router>
