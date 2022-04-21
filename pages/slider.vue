<template>
  <div class="container">
    <client-only>
      <vue-tiny-slider v-bind="tinySliderOptions">
        <div class="card-container" v-for="(product, i) of productsData" :key="i">
          <div class="card">
            <img class="card-img-top" :src=product.productAsset.preview  alt="product-card-img"/>
            <div class="card-body">
              <a class="card-link">
                <h4 class="card-title">{{ product.productName }}</h4>
              </a>
              <div class="card-text">
                <strong>{{ product.price.max }}</strong>
                <br>
                <span>including TAX</span>
              </div>
            </div>
          </div>
        </div>
      </vue-tiny-slider>
    </client-only>
  </div>
</template>

<script>

export default {
  name: 'slider',
  components: {
  },
  data() {
    return {
      sortType: 'Default',
      tinySliderOptions: {
        autoplay: true,
        autoplayButtonOutput: false,
        loop: false,
        mouseDrag: true,
        items: 1,
        swipeAngle: 45,
        gutter: 10,
        responsive: {
          576: {
            items: 2
          },
          768: {
            items: 3
          },
          992: {
            items: 4
          }
        }
      },
      productsData: [
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/canon.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/galaxy.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Weldgalaxy X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/headphone.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/ipad.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/macbook-pro.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/pixel.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/watch.jpg" },
          productId: '55',
          slug: 'brick'
        },
        {
          productName: "Engweld X-Pert S150 mma Inverter",
          price: { max: "£909.90" },
          productAsset: { preview:"/images/slider/macbook-air.jpg" },
          productId: '55',
          slug: 'brick'
        },
      ],
    };
  },
}
</script>

<style scoped>
.card-container {
  padding: 0 0 25px 0;
}
.card {
  width: 100%;
  box-shadow: 0 4px 30px rgba(39, 42, 84, 0.16);
  border-radius: 8px;
  border: 1px solid #D8E2EF;
}
.card-img-top {
  width: 100%;
  height: 200px;
  object-fit: contain;
  border-radius: 8px 8px 0 0;
  background: #F7F7F7;
}
.card-link {
  text-decoration: none;
}

.card-title {
  overflow: hidden;
  text-overflow: ellipsis;
  height: 70px;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 22px;
  color: orange;
}

.card-title:hover {
   cursor: pointer;
   color: #3A4ABF;
 }

.card-text strong {
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 24px;
  color: #FE4B49;
}
.card-text span {
  font-style: normal;
  font-weight: 400;
  font-size: 13px;
  line-height: 16px;
  color: #1A2942;
}
</style>
