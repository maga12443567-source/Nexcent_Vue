<script setup>
// core version + navigation, pagination modules:
import Swiper from "swiper";
import { Navigation, Pagination } from "swiper/modules";
// import Swiper and modules styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { onMounted } from "vue";

onMounted(() => {
  const swiper = new Swiper(".manage-swiper", {
    modules: [Navigation, Pagination],
    slidesPerView: 1,
    spaceBetween: 10,
    breakpoints: {
      576: {
        slidesPerView: 1,
        spaceBetween: 24,
      },
      768: {
        slidesPerView: 3,
        spaceBetween: 24,
      },
    },
    pagination: {
      el: ".swiper-pagination",
      clickable: true,
    },
    navigation: {
      nextEl: ".swiper-button-next",
      prevEl: ".swiper-button-prev",
    },
  });
});
</script>

<template>
  <section class="manage">
    <div class="container">
      <h2>
        Manage your entire community <br />
        in a single system
      </h2>
      <p class="manage__subtitle">Who is Nextcent suitable for?</p>
      <div class="swiper manage-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <div class="manage__card h-100">
              <div class="manage__card-icon">
                <img src="@/assets/img/manage-1.svg" alt="" />
              </div>
              <h4>Membership Organisations</h4>
              <p>
                Our membership management software provides full automation of membership renewals
                and payments
              </p>
            </div>
          </div>
          <div class="swiper-slide">
            <div class="manage__card h-100">
              <div class="manage__card-icon">
                <img src="@/assets/img/manage-2.svg" alt="" />
              </div>
              <h4>National Associations</h4>
              <p>
                Our membership management software provides full automation of membership renewals
                and payments
              </p>
            </div>
          </div>
          <div class="swiper-slide">
            <div class="manage__card h-100">
              <div class="manage__card-icon">
                <img src="@/assets/img/manage-3.svg" alt="" />
              </div>
              <h4>Clubs & Groups</h4>
              <p>
                Our membership management software provides full automation of membership renewals
                and payments
              </p>
            </div>
          </div>
        </div>
        <div class="swiper-pagination"></div>
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>
    </div>
  </section>
</template>
