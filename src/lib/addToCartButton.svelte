
<script lang="ts">
     import {cartItems, addToCart, removeFromCart } from "./buttons/cart";

     const products = [
        {
          id: 1,
          name: "Simple Indian Curry",
          image: "",
          desc: "",
          price: 14.99,
        },
        {
          id: 2,
          name: "Mexican Tacos",
          image: "",
          desc: "",
          price: 14.99,
        },
        {
          id: 3,
          name: "Fish",
          image: "",
          desc: "",
          price: 14.99,
        },
      ];

</script>


<div class="grid">
    {#each products as product}
      <div class="card">
        <h3>{product.name}</h3>
        <img src={product.image} alt="image">
        <p>{product.desc}</p>
        <p>Price: ${product.price}</p>
        <button on:click={() => addToCart(product)}>Add to cart</button>
      </div>
    {/each}
  </div>

  <style>
      .grid {
        display: grid;
        grid-gap: 1em;
        margin-bottom: 5em;
        grid-template-columns: repeat(3, 1fr);
      }
    
    
      .card {
        background-color: orangered;
        border-radius: 10px;
        color: white;
        padding-left: .5em;
      }
      button {
        width: 50%;
        padding: 0.5em 1em;
        float: right;
      }
    </style>
    