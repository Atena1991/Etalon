<template>
    <body>
        <Header/>
        <Navbar/>
        <main>
            <BrandCooperation/>
            <NewCollection/>
            <BestSeller/>
        </main>
        <Footer/>
    </body>
</template>
<script>
    import Header from './components/Header.vue'
    import Navbar from './components/Navbar.vue'
    import BrandCooperation from './components/BrandCooperation.vue'
    import NewCollection from './components/NewCollection.vue'
    import BestSeller from './components/BestSeller.vue'
    import Footer from './components/Footer.vue'

    export default {
        name:"App",
        components:{
            Header,
            Navbar,
            BrandCooperation,
            NewCollection,
            BestSeller,
            Footer
        }
    }
</script>
<!-- <style scoped>
.btn {
  font-size: var(--fs-btn);
  border-radius: 6px;
}
.btn-yellow {
  background: var(--secondary-background-color);
  color: var(--fc-dark);
}
.btn-yellow:hover {
  background: #FFEB9D;
}
.btn-black,
.btn-black2 {
  background: #181818;  
  color: var(--fc-light);
  padding: 16px 40px;
  line-height: 17px;
}
.btn-black:hover {
  background: #1E1E1E;
  color: #FFFFFF;
}
.btn-black2:hover {
  background: #1E1E1E;
  color: #FFFFFF;
} 
.shoes{
  z-index:3 ;
}
</style> -->



