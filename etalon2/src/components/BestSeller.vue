<template>
<section class="best-seller">
    <div class="container">
        <h3 class="text-capitalize">Best Sellers</h3>
        <ul class="row flex-nowrap list-unstyled overflow-auto">
            <li class="col">
                <div class="card">
                    <span class="percent d-none d-md-block d-lg-none"></span>
                    <span class="icon icon-heart"></span>
                    <img class="product-img" src="src/assets/images/backpack.svg" alt="bagpack">
                </div>
                <div class="d-flex ">
                    <div class="col-10 position-relative">
                        <p class="sub ">Fjallraven Backpack</p>
                        <p><span class="price d-md-none d-lg-block mb-0 ">$109.95</span></p>
                        <p><span class="price new-price position-absolute d-none d-md-block d-lg-none" ><rubby class="opacity-25 text-decoration-line-through me-2">$157</rubby>$109.95</span></p>
                    </div>
                    <span @click="increment" class="cart new-pos align-self-center text-end col-1"><img src="src/assets/images/cart-square.svg"></span>
                </div>
            </li>
            <li class="col">
                <div class="card">
                    <span class="icon icon-heart"></span>
                    <img class="product-img" src="src/assets/images/beige-coat.svg" alt="beige-coat">
                </div>
                <div class="d-flex">
                    <div class="col-10">
                        <p class="sub">Mens Cotton Jacket</p>
                        <p><span class="price">$55.99</span></p>
                    </div>
                    <span @click="increment" class="cart align-self-center text-end col-1"><img src="src/assets/images/cart-square.svg"></span>
                </div>
            </li>
            <li class="col">
                <div class="card">
                    <span class="icon icon-heart"></span>
                    <img class="product-img" src="src/assets/images/white-shirt.svg" alt="slim-fit-tshirt">
                </div>
                <div class="d-flex">
                    <div class="col-10">
                        <p class="sub">Slim Fit T-Shirts</p>
                        <p><span class="price">$22.3</span></p>
                    </div>
                    <span @click="increment" class="cart align-self-center text-end col-1"><img src="src/assets/images/cart-square.svg"></span>
                </div>
            </li>
            <li class="col">
                <div class="card">
                    <span class="percent"></span>
                    <span class="icon icon-heart"></span>
                    <img class="product-img" src="src/assets/images/blue-shirt.svg" alt="casual-slim-fit">
                </div>
                <div class="d-flex">
                    <div class="col-10">
                        <p class="sub">Mens Casual Slim Fit</p>
                        <p><span class="price"><rubby class="opacity-25 text-decoration-line-through me-2">$15.99</rubby>$11.25</span></p>
                    </div>
                    <span @click="increment" class="cart align-self-center text-end col-1"><img src="src/assets/images/cart-square.svg"></span>
                </div>
            </li>
        </ul>
    </div>
    <div class="text-center pb-5 d-none d-lg-block d-xl-block d-xxl-block">
        <a class="btn btn-black2"  href="#" title="more-product"> Load More Products</a>
    </div>
</section>
</template>
<script>
     import { mapActions, mapStores } from 'pinia';
    import { useCounterStore } from '@/stores/counter'

    export default {
    computed: {
        ...mapStores(useCounterStore)
    } ,
    methods: {
        ...mapActions(useCounterStore, ['increment'])
    }
    }
</script>
<!-- <style scoped>

.best-seller {
  background: var(--primary-background-color);
}
.card {
  background: var(--white-background-color);
  position: relative;
  border-radius: 24px;
  height: clamp(220px, 50vw, 347px);
}
.icon {
  display: inline-block;
  position: absolute;
  padding: 12px;
  width: 24.01px;
  height: 21.1px;
  background-size: cover;
  top: 17.92px;
  right: 15.75px;
}
.icon-heart {
  background-image: url(../images/heart-light.svg);
}
.icon-heart:hover,
.icon-heart:focus {
  background-image: url(../images/heart-black.svg);
  cursor: pointer;
  transition: all 0.6 ease;
}
.percent {
  display: inline-block;
  position: absolute;
  width: 41px;
  height: 20px;
  background-size: cover;
  background-image: url(../images/30off.svg);
  top: 17.92px;
  left: 16px;
}
.product-img {
  object-position: center;
  margin-inline: auto;
  padding-top: 54.01px ;
  padding-bottom: 54.01px;
}
.sub {
  font-family: var(--secondary-font-family);
  font-size: var(--fs-sm);
  font-weight: 500;
  line-height: 21px;
  margin-top: 16px;
  margin-bottom: 0;
}
.price {
  font-family: var(--secondary-font-family);
  font-size: var(--fs-price);
  font-weight: 300;
  line-height: 19px;
  color: rgba(0, 0, 0, 0.6);
  margin-top: 4px;
  margin-bottom: 32px;
}
.new-price {
 top: 37px;
 left: 0;
}
</style> -->
