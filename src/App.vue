<template>
  <div class="page" @scroll="onScroll">
    <div class="intro">
      <div
        :class="{ active: menu, transform: menuTransfrom }"
        class="menu intro__menu"
      >
        <img class="logo menu__logo" src="@/assets/logo-fill.png" alt="" />

        <a
          :class="{ active: menu }"
          @click.prevent="menu = !menu"
          class="menu__link"
          href="#"
        >
          меню <span></span>
        </a>

        <div :class="{ 'sublist-open': sublist }" class="menu__inner">
          <img class="logo" src="@/assets/logo-fill.png" alt="logo" />

          <ul class="menu__list menu-list">
            <li class="menu-list__item">
              <a @click="onSublist" class="menu-list__link" href="#"
                >Тепличные комплексы</a
              >

              <ul class="menu__sublist menu-sublist">
                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">ТК Сосногорский</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">ТК Новочебоксарский</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">ТК Пермский</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">тк камчатский</a>
                </li>
              </ul>
            </li>

            <li class="menu-list__item">
              <a @click="onSublist" class="menu-list__link" href="#"
                >Компания</a
              >

              <ul class="menu__sublist menu-sublist">
                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">Lorem, ipsum dolor.</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">Lorem, ipsum.</a>
                </li>
              </ul>
            </li>

            <li class="menu-list__item">
              <a @click="onSublist" class="menu-list__link" href="#">Бренды</a>

              <ul class="menu__sublist menu-sublist">
                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">Lorem</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">ipsum</a>
                </li>

                <li class="menu-sublist__item">
                  <a class="menu-sublist__link" href="#">content</a>
                </li>
              </ul>
            </li>

            <li class="menu-list__item">
              <a class="menu-list__link" href="#">Вакансии</a>
            </li>

            <li class="menu-list__item">
              <a class="menu-list__link" href="#">Закупки</a>
            </li>

            <li class="menu-list__item">
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
              <a class="menu-contacts__telegram" href="#">
                <img src="@/assets/icons/telegram.svg" alt="telegram" />
              </a>
              <a class="menu-contacts__vk" href="#">
                <img src="@/assets/icons/vk.svg" alt="vk" />
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="intro__inner container">
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
        <div class="about__video about-video">
          <h2 class="about__title title">о Компании</h2>
          <i @click="videoModal = true" class="about-video__btn">
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

      <div
        @click="videoModal = false"
        :class="{ open: videoModal }"
        class="modal-video__backdrop"
      ></div>
      <div :class="{ open: videoModal }" class="modal-video">
        <video
          class="modal-video__video"
          src="@/assets/about-video.mp4"
          controls
        ></video>
        <div @click="videoModal = false" class="modal-video__close"></div>
      </div>
    </div>

    <div class="brands">
      <div class="brands__inner container">
        <div class="brands__heading">
          <h2 class="brands__title title">наши <span>бренды</span></h2>
        </div>
        <div class="brands__content">
          <Swiper
            :slides-per-view="mobile ? 1 : 2"
            :space-between="140"
            :modules="[Navigation]"
            navigation
            class="brands-swiper"
          >
            <SwiperSlide
              v-for="slide in 28"
              :key="slide"
              class="brands-swiper__slide"
            >
              <img src="@/assets/swiper/01.png" alt="" />
            </SwiperSlide>
          </Swiper>

          <p class="brands__text">
            «Спелые витамины» - торговая марка, под которой ГК «Теплицы
            Регионов» производит вкусные, наполненные витаминами томаты и
            огурцы. В основе бренда лежит качество продукции, ее полезные
            свойства и польза. Бренд только начинает развиваться, но уже
            достаточно хорошо известен в регионах выращивания.
          </p>
          <a class="brands__btn button" href="#">Подробнее</a>
        </div>
      </div>
    </div>

    <div class="complexes">
      <div class="complexes__inner container">
        <div class="complexes__top">
          <h2 class="title complexes__title">
            тепличные <span>комплексы</span>
          </h2>
          <div class="complexes__items">
            <div class="complexes__item">
              <div class="complexes__num">4</div>
              <div class="complexes__text">Тепличных комплекса</div>
            </div>

            <div class="complexes__item">
              <div class="complexes__num">60 га</div>
              <div class="complexes__text">Общая площадь теплиц</div>
            </div>

            <div class="complexes__item">
              <div class="complexes__num">55 000</div>
              <div class="complexes__text">Тонн продукции в год</div>
            </div>
          </div>
        </div>
        <div class="complexes__content">
          <div :class="{ 'sheet-modal': mobile }" class="complexes__main">
            <div class="complexes__image">
              <a href="#" class="button complexes__btn">Подробнее</a>
            </div>
            <div class="complexes__main-inner">
              <div class="complexes__name">{{ currentComplex.name }}</div>
              <div class="complexes__text">
                {{ currentComplex.text }}
              </div>
              <div class="complexes__info complexes-info">
                <div class="complexes-info__item">
                  <div class="complexes-info__num">23,5 <span>га</span></div>
                  <div class="complexes-info__text">
                    площадь <br />
                    теплиц
                  </div>
                </div>

                <div class="complexes-info__item">
                  <div class="complexes-info__num">6 <span>сортов</span></div>
                  <div class="complexes-info__text">
                    помидоров <br />
                    и огурцов
                  </div>
                </div>

                <div class="complexes-info__item">
                  <div class="complexes-info__num">
                    22 000 <span>тонн</span>
                  </div>
                  <div class="complexes-info__text">
                    продукции <br />
                    в год
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div
            @click="currentComplex = complexes[0]"
            :class="{ active: currentComplex.id === 1 }"
            class="active complexes__marker complexes-marker complexes-marker-1"
          >
            <i class="complexes-marker__icon">
              <svg
                width="89"
                height="165"
                viewBox="0 0 89 165"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  class="marker"
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  fill="#F4A62F"
                />
                <path
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  stroke="white"
                />
                <ellipse
                  cx="64.9274"
                  cy="19.5801"
                  rx="8.68073"
                  ry="8.79771"
                  fill="#FCFCFC"
                  fill-opacity="0.22"
                />
                <g clip-path="url(#clip0_5_8516)">
                  <path
                    d="M29.8063 147.959C37.8181 151.43 48.9814 143.172 54.7406 129.52C60.5014 115.865 64.889 64.7982 64.889 64.7982C64.889 64.7982 31.4916 103.295 25.7308 116.95C19.9715 130.602 21.7976 144.488 29.8063 147.959V147.959Z"
                    fill="url(#paint0_linear_5_8516)"
                    fill-opacity="0.15"
                  />
                </g>
                <defs>
                  <linearGradient
                    id="paint0_linear_5_8516"
                    x1="29.8058"
                    y1="147.958"
                    x2="65.69"
                    y2="65.1453"
                    gradientUnits="userSpaceOnUse"
                  >
                    <stop stop-color="#414141" stop-opacity="0" />
                    <stop offset="1" stop-color="#414141" />
                  </linearGradient>
                  <clipPath id="clip0_5_8516">
                    <rect
                      width="55.9718"
                      height="96.8431"
                      fill="white"
                      transform="matrix(-0.917562 -0.397593 0.388695 -0.921366 51.3576 165)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </i>
            <div class="complexes-marker__label">{{ currentComplex.name }}</div>
          </div>

          <div
            @click="currentComplex = complexes[1]"
            :class="{ active: currentComplex.id === 2 }"
            class="complexes__marker complexes-marker complexes-marker-2"
          >
            <i class="complexes-marker__icon">
              <svg
                width="89"
                height="165"
                viewBox="0 0 89 165"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  class="marker"
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  fill="#F4A62F"
                />
                <path
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  stroke="white"
                />
                <ellipse
                  cx="64.9274"
                  cy="19.5801"
                  rx="8.68073"
                  ry="8.79771"
                  fill="#FCFCFC"
                  fill-opacity="0.22"
                />
                <g clip-path="url(#clip0_5_8516)">
                  <path
                    d="M29.8063 147.959C37.8181 151.43 48.9814 143.172 54.7406 129.52C60.5014 115.865 64.889 64.7982 64.889 64.7982C64.889 64.7982 31.4916 103.295 25.7308 116.95C19.9715 130.602 21.7976 144.488 29.8063 147.959V147.959Z"
                    fill="url(#paint0_linear_5_8516)"
                    fill-opacity="0.15"
                  />
                </g>
                <defs>
                  <linearGradient
                    id="paint0_linear_5_8516"
                    x1="29.8058"
                    y1="147.958"
                    x2="65.69"
                    y2="65.1453"
                    gradientUnits="userSpaceOnUse"
                  >
                    <stop stop-color="#414141" stop-opacity="0" />
                    <stop offset="1" stop-color="#414141" />
                  </linearGradient>
                  <clipPath id="clip0_5_8516">
                    <rect
                      width="55.9718"
                      height="96.8431"
                      fill="white"
                      transform="matrix(-0.917562 -0.397593 0.388695 -0.921366 51.3576 165)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </i>
            <div class="complexes-marker__label">{{ currentComplex.name }}</div>
          </div>

          <div
            @click="currentComplex = complexes[2]"
            :class="{ active: currentComplex.id === 3 }"
            class="complexes__marker complexes-marker complexes-marker-3"
          >
            <i class="complexes-marker__icon">
              <svg
                width="89"
                height="165"
                viewBox="0 0 89 165"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  class="marker"
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  fill="#F4A62F"
                />
                <path
                  d="M64.9744 0C54.3968 0 45.8248 8.61295 45.8248 19.2334C45.8248 29.8565 64.9744 64.6943 64.9744 64.6943C64.9744 64.6943 84.1253 29.8565 84.1253 19.2334C84.1253 8.61295 75.5479 0 64.9744 0Z"
                  stroke="white"
                />
                <ellipse
                  cx="64.9274"
                  cy="19.5801"
                  rx="8.68073"
                  ry="8.79771"
                  fill="#FCFCFC"
                  fill-opacity="0.22"
                />
                <g clip-path="url(#clip0_5_8516)">
                  <path
                    d="M29.8063 147.959C37.8181 151.43 48.9814 143.172 54.7406 129.52C60.5014 115.865 64.889 64.7982 64.889 64.7982C64.889 64.7982 31.4916 103.295 25.7308 116.95C19.9715 130.602 21.7976 144.488 29.8063 147.959V147.959Z"
                    fill="url(#paint0_linear_5_8516)"
                    fill-opacity="0.15"
                  />
                </g>
                <defs>
                  <linearGradient
                    id="paint0_linear_5_8516"
                    x1="29.8058"
                    y1="147.958"
                    x2="65.69"
                    y2="65.1453"
                    gradientUnits="userSpaceOnUse"
                  >
                    <stop stop-color="#414141" stop-opacity="0" />
                    <stop offset="1" stop-color="#414141" />
                  </linearGradient>
                  <clipPath id="clip0_5_8516">
                    <rect
                      width="55.9718"
                      height="96.8431"
                      fill="white"
                      transform="matrix(-0.917562 -0.397593 0.388695 -0.921366 51.3576 165)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </i>
            <div class="complexes-marker__label">{{ currentComplex.name }}</div>
          </div>
        </div>
      </div>
    </div>

    <div class="vacancies">
      <div class="vacancies__inner container">
        <div class="vacancies__heading">
          <h2 class="title vacancies__title">работа <span>в теплицах</span></h2>
        </div>
        <div class="vacancies__content">
          <img
            class="vacancies__bg"
            src="@/assets/vacancies-title.png"
            alt=""
          />
          <p class="vacancies__text">
            Гарантируем достойный уровень заработной платы, <br />
            оформление по ТК РФ, удобный рабочий график <br />
            и возможность Вашего карьерного продвижения <br />
            и профессионального развития.
          </p>
          <div class="vacancies__items">
            <div class="vacancies__item vacancies-item">
              <div class="vacancies-item__num">16</div>
              <div class="vacancies-item__label">Открытых вакансий</div>
              <a href="#" class="vacancies-item__link"></a>
            </div>

            <div class="vacancies__item vacancies-item">
              <div class="vacancies-item__num">40</div>
              <div class="vacancies-item__label">Вакансий в банке</div>
              <div class="vacancies-item__text">
                Вы можете быть полезны <br />
                нам в будущем!
              </div>
              <a href="#" class="vacancies-item__link"></a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="purchases">
      <div class="purchases__inner container">
        <div class="purchases__heading">
          <h2 class="title purchases__title">закупки</h2>
        </div>
        <div class="purchases__content">
          <p class="purchases__text">
            Мы готовы рассмотреть интересные коммерческие предложения <br />
            по оптовой закупке удобрений, средств защиты растений, офисной
            <br />
            техники, спецодежды и других товаров.
          </p>
          <a href="#" class="button purchases__btn">На страницу закупок</a>

          <img class="purchases__bg" src="@/assets/purchases-bg.png" alt="" />
        </div>
      </div>
    </div>

    <div class="partners">
      <div class="partners__inner container">
        <h2 class="title partners__title">партнеры</h2>
        <Swiper
          :space-between="mobile ? '20' : '80'"
          :modules="[Navigation]"
          :navigation="mobile ? false : true"
          class="partners-swiper"
        >
          <SwiperSlide
            v-for="slide in 28"
            :key="slide"
            class="partners-swiper__slide"
          >
            <img src="@/assets/partners-slide-01.png" alt="" />
          </SwiperSlide>
        </Swiper>
      </div>
    </div>

    <footer class="footer">
      <div class="footer__inner container">
        <div class="footer__copyright footer-copyright">
          <div class="footer-copyright__text">© 2008-2020 text.</div>
          <div class="footer-copyright__text">
            Сайт сделан: Reka Digital Agency
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

const menu = ref(false);
const menuTransfrom = ref(false);
const sublist = ref(false);
const videoModal = ref(false);

const mobile = ref(false);

onMounted(() => {
  window.innerWidth < 380 ? (mobile.value = true) : (mobile.value = false);

  window.addEventListener("resize", function (e) {
    e.target.innerWidth < 380 ? (mobile.value = true) : (mobile.value = false);
  });
});

const complexes = [
  {
    id: 1,
    name: "ТК Сосногорский",
    text: "Тепличный комплекс «Новочебоксарский» — это первая производственная площадка холдинга, запущенная в работу в 2019 году. ",
  },
  {
    id: 2,
    name: "Lorem ipsum 1",
    text: "Lorem ipsum dolor sit amet consectetur adipisicing.",
  },
  {
    id: 3,
    name: "Lorem ipsum 2",
    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestiae possimus cum fuga.",
  },
];

const currentComplex = ref(complexes[0]);

const onScroll = (e) => {
  e.target.scrollTop >= 979
    ? (menuTransfrom.value = true)
    : e.target.scrollTop < 650
    ? (menuTransfrom.value = false)
    : "";
};

const onSublist = (item) => {
  const items = Array.from(item.target.offsetParent.offsetParent.children);
  const targetItem = item.target.offsetParent;

  sublist.value = true;

  if (targetItem.classList.contains("active")) {
    targetItem.classList.remove("active");
    sublist.value = false;
  } else {
    items.map((elem) => elem.classList.remove("active"));
    targetItem.classList.add("active");
  }
};
const skipIntro = () => {
  const page = document.querySelector(".page");
  const introHeight = document.querySelector(".intro").offsetHeight;

  page.scroll({
    top: introHeight,
    behavior: "smooth",
  });
};
</script>
