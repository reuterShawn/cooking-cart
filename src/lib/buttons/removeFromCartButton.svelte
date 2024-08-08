<script>
         import {cartItems, addToCart, removeFromCart } from "./cart";

</script>
src/routes/cart.ts

{#if $cartItems.length > 0}
<h1>Cart</h1>

<div class="grid">
  {#each $cartItems as cartItem}
    <div>
      <h2>{cartItem.name}</h2>
      <p>Amount: {cartItem.amount}</p>
      <p>Price: ${cartItem.price}</p>
      <p>Total: ${cartItem.price * cartItem.amount}</p>
      <button on:click={() => removeFromCart(cartItem.id)}
        >Remove from cart</button
      >
    </div>
  {/each}
</div>
{/if}


<style>
    main {
      margin: 0 auto;
      max-width: 54em;
    }
  
    .grid {
      display: grid;
      grid-gap: 1em;
      margin-bottom: 5em;
      grid-template-columns: repeat(3, 1fr);
    }
  
    h1 {
      padding-bottom: 0.5em;
      border-bottom: 2px dotted black;
    }
  
    button {
      width: 100%;
      padding: 0.5em 1em;
    }
  </style>
  