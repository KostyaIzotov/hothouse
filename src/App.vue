<template>
  <div class="intro">
    <div class="intro__inner container">
      <div :class="{ active: menu }" class="menu intro__menu">
        <a
          :class="{ active: menu }"
          @click="menu = !menu"
          class="menu__link"
          href="#"
        >
          меню <span></span>
        </a>

        <div :class="{ 'sublist-open': sublist }" class="menu__inner">
          <img class="logo" src="@/assets/logo-fill.png" alt="logo" />

          <ul class="menu__list menu-list">
            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Тепличные комплексы</a>

              <ul class="menu-list menu__sublist menu-sublist">
                <li class="menu-list__item menu-sublist__item">
                  <a class="menu-list__link menu-sublist__link" href="#"
                    >ТК Сосногорский</a
                  >
                </li>

                <li class="menu-list__item menu-sublist__item">
                  <a class="menu-list__link menu-sublist__link" href="#"
                    >ТК Новочебоксарский</a
                  >
                </li>

                <li class="menu-list__item menu-sublist__item">
                  <a class="menu-list__link menu-sublist__link" href="#"
                    >ТК Пермский</a
                  >
                </li>

                <li class="menu-list__item menu-sublist__item">
                  <a class="menu-list__link menu-sublist__link" href="#"
                    >тк камчатский</a
                  >
                </li>
              </ul>
            </li>

            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Компания</a>
            </li>

            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Бренды</a>
            </li>

            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Вакансии</a>
            </li>

            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Закупки</a>
            </li>

            <li @click="onSublist" class="menu-list__item">
              <a class="menu-list__link" href="#">Контакты</a>
            </li>
          </ul>

          <div class="menu__contacts menu-contacts">
            <div class="menu-contacts__top">
              <a class="menu-contacts__phone" href="+79876543210">
                +7 987 654 32 10
              </a>
              <a class="menu-contacts__mail" href="mailto:info@agro-man.ru">
                info@agro-man.ru
              </a>
            </div>
            <div class="menu-contacts__socials">
              <a href="#">
                <img src="@/assets/icons/telegram.svg" alt="telegram" />
              </a>
              <a href="#">
                <img src="@/assets/icons/vk.svg" alt="vk" />
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="intro__main">
        <img class="logo intro__logo" src="@/assets/logo.png" alt="logo" />
        <div class="intro__heading">
          <h1 class="intro__title">
            теплицы <br />
            регионов
          </h1>
          <h4 class="intro__subtitle">
            Тепличные комплексы <br />
            современного <br />
            поколения
          </h4>
        </div>

        <div class="intro__about intro-about">
          <div class="intro-about__top">
            <img
              class="intro-about__icon"
              src="@/assets/icons/intro-about.svg"
              alt=""
            />
            <span class="intro-about__label"
              >Знак качества <br />
              xxi века</span
            >
          </div>
          <a class="intro-about__btn button" href="#">О компании</a>
        </div>
      </div>

      <div @click="skipIntro" class="intro-skip">
        <span></span>
        <svg
          width="21"
          height="14"
          viewBox="0 0 21 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M3.50165 0L0 3.49938L10.5 14L21 3.49938L17.4984 0L10.5 7.00123L3.50165 0Z"
            fill="white"
          />
        </svg>
      </div>
    </div>
  </div>

  <div class="about">
    <div class="about__inner container">
      <div class="about__video about-video block-image">
        <h2 class="about__title title">о Компании</h2>
        <i class="about-video__btn">
          <svg
            width="138"
            height="120"
            viewBox="0 0 138 120"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1 105V36.6342C1 30.7949 4.62426 25.5689 10.0931 23.5223L65.1037 2.93569C68.3155 1.73377 71.8566 1.75244 75.0555 2.98817L128.045 23.458C133.442 25.5428 137 30.7322 137 36.5175V105C137 112.732 130.732 119 123 119H15C7.26801 119 1 112.732 1 105Z"
              stroke="white"
              stroke-width="2"
            />
            <path
              d="M96 64.0001C97.3333 64.7699 97.3333 66.6944 96 67.4642L57 89.9809C55.6667 90.7507 54 89.7884 54 88.2488L54 43.2155C54 41.6759 55.6667 40.7137 57 41.4835L96 64.0001Z"
              fill="white"
            />
          </svg>
        </i>
      </div>
      <div class="about__content">
        <p class="about__text">
          «Теплицы Регионов» - группа компаний, создающая и управляющая
          высокотехнологичными тепличными комплексами для круглогодичного
          выращивания овощной продукции. Самые передовые и инновационные
          разработки отрасли круглогодичного выращивания овощной продукции в
          защищенном (закрытом) грунте апробируются и применяются на
          производствах компании.
        </p>

        <div class="about__items">
          <div class="about__item about-item">
            <div class="about-item__num">4</div>
            <div class="about-item__text">региона выращивания</div>
          </div>

          <div class="about__item about-item">
            <div class="about-item__num">60 га</div>
            <div class="about-item__text">общая площадь теплиц</div>
          </div>

          <div class="about__item about-item">
            <div class="about-item__num">1 300</div>
            <div class="about-item__text">сотрудников</div>
          </div>

          <div class="about__item about-item">
            <div class="about-item__num">55 000</div>
            <div class="about-item__text">тонн продукции в год</div>
          </div>
        </div>

        <a class="about__btn button" href="#">Подробнее</a>
      </div>
    </div>
  </div>

  <div class="brands">
    <div class="brands__inner container">
      <div class="brands__heading block-image">
        <h2 class="brands__title title">наши <span>бренды</span></h2>
      </div>
      <div class="brands__content">
        <swiper
          :slides-per-view="1"
          :space-between="50"
          :modules="[Navigation]"
          navigation
        >
          <swiper-slide>
            <img src="@/assets/swiper/01.png" alt="" />
          </swiper-slide>
          <swiper-slide>
            <img src="@/assets/swiper/01.png" alt="" />
          </swiper-slide>
          <swiper-slide>
            <img src="@/assets/swiper/01.png" alt="" />
          </swiper-slide>
        </swiper>

        <p class="brands__text">
          «Спелые витамины» - торговая марка, под которой ГК «Теплицы Регионов»
          производит вкусные, наполненные витаминами томаты и огурцы. В основе
          бренда лежит качество продукции, ее полезные свойства и польза. Бренд
          только начинает развиваться, но уже достаточно хорошо известен в
          регионах выращивания.
        </p>
        <a class="brands__btn button" href="#">Подробнее</a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css/bundle";

const menu = ref(false);
const sublist = ref(false);

const onSublist = (item) => {
  const items = item.target.offsetParent.offsetParent.children;

  if (item.target.offsetParent.classList.contains("active")) {
    item.target.offsetParent.classList.remove("active");
    sublist.value = false;
  }

  for (let el of items) {
    el.classList.remove("active");
    sublist.value = false;
  }

  item.target.offsetParent.classList.toggle("active");
  sublist.value = true;
};
const skipIntro = () => {
  const introHeight = document.querySelector(".intro").offsetHeight;

  window.scroll({
    top: introHeight,
    behavior: "smooth",
  });
};
</script>
