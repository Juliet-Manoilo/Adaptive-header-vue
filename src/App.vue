<template>
  <header class="header">
    <div class="header__top-panel">
      <div class="hamburger-menu">
        <input id="menu__toggle" type="checkbox" />
        <label class="menu__btn" for="menu__toggle">
          <span></span>
        </label>

        <ul class="menu__box">
          <li>
            <a class="menu__item" href="#"
              ><i class="fas fa-sign-in-alt"></i>Личный кабинет</a
            >
          </li>
          <li>
            <a class="menu__item" href="#"
              ><i class="fas fa-phone-alt"></i>9-800-888-88-88 (заказать
              звонок)</a
            >
          </li>
          <li>
            <a class="menu__item" href="#"
              ><i class="far fa-envelope"></i>info@petsy.com</a
            >
          </li>
          <li>
            <a class="menu__item" href="#"
              ><i class="far fa-heart"></i>Избранное</a
            >
          </li>
          <li><a class="menu__item" href="#">О компании</a></li>
          <li><a class="menu__item" href="#">Сотрудничество</a></li>
          <li><a class="menu__item" href="#">Оплата и доставка</a></li>
          <li><a class="menu__item" href="#">Контакты</a></li>
          <form action="#" method="POST" class="header__form--burger">
            <input type="search" class="header__input" />
            <button type="submit" class="header__btn">
              <i class="fas fa-search"></i>
            </button>
          </form>
        </ul>
      </div>
      <a href="mailto:x@yoursite.com" class="header__contacts-link"
        ><i class="far fa-envelope"></i>info@petsy.com</a
      >
      <a href="#" class="header__contacts-link"
        ><i class="fas fa-phone-alt"></i>9-800-888-88-88 (заказать звонок)</a
      >
      <a href="/" class="header__contacts-link--bold"
        >Интернет-магазин товаров для животных</a
      >
      <a href="#" class="header__contacts-link"
        ><i class="fas fa-sign-in-alt"></i>Личный кабинет</a
      >
      <a href="#" class="header__contacts-link"
        ><i class="far fa-heart"></i>Избранное</a
      >
    </div>
    <div class="header__nav-panel">
      <a href="/" class="header__logo">logo</a>
      <nav class="header__nav">
        <a href="#" class="header__nav-link">Оплата и доставка</a>
        <a href="#" class="header__nav-link">Контакты</a>
        <a href="#" class="header__nav-link">О компании</a>
        <a href="#" class="header__nav-link">Сотрудничество</a>
      </nav>
      <form action="#" method="POST" class="header__form">
        <input type="search" class="header__input" />
        <button type="submit" class="header__btn">
          <i class="fas fa-search"></i>
        </button>
      </form>
      <div class="header__basket">
        <span class="header__sum">15000₽</span>
        <span class="header__quantity">(6)</span>
        <a href="#" class="header__basket-link"
          ><i class="fas fa-shopping-basket"></i
        ></a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Roboto:wght@400;700&display=swap");

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
  color: inherit;
  display: inline-block;
}

i {
  margin-right: 10px;
}

.header {
  min-height: 25vh;
  width: 100%;
  border-top: 2px solid black;
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  @media (max-width: 1200px) {
    font-size: 14px;
  }
  &__top-panel {
    height: 80px;
    background-color: #84c7ff;
    padding: 0 5% 0 5%;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    @media (max-width: 992px) {
      justify-content: center;
    }
  }
  &__contacts-link {
    padding: 5px 0;
    @media (max-width: 992px) {
      display: none;
    }
    &--bold {
      padding: 5px 25px;
      font-weight: bold;
      @media (max-width: 992px) {
        font-size: 16px;
        width: 60%;
        text-align: center;
      }
      &:hover {
        transform: scale(1.1);
        transition: 0.3s ease;
      }
    }
    &:hover {
      transform: scale(1.1);
      transition: 0.2s ease;
    }
  }
  &__nav-panel {
    padding: 0 5% 0 5%;
    color: black;
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    @media (max-width: 992px) {
      flex-direction: column;
      align-items: center;
    }
  }
  &__logo {
    font-family: "Dancing Script", cursive;
    font-size: 98px;
    color: palevioletred;
    margin-right: 50px;
    text-transform: uppercase;
    @media (max-width: 992px) {
      font-size: 72px;
      margin-right: 0;
    }
  }
  &__nav {
    display: inline-flex;
    min-width: 50%;
    justify-content: space-around;
    height: 100%;
    align-items: center;
    @media (max-width: 992px) {
      display: none;
    }
  }
  &__nav-link:hover {
    opacity: 0.8;
  }
  &__input {
    border: 1px solid gray;
    border-radius: 15px;
    height: 30px;
    outline: none;
    padding-left: 10px;
  }
  &__form {
    outline: none;
    border: none;
    display: flex;
    position: relative;
    @media (max-width: 992px) {
      display: none;
    }
    &--burger {
      padding-left: 20px;
    }
  }
  &__btn {
    outline: none;
    color: gray;
    border: none;
    background-color: transparent;
    transform: translate(-100%);
    cursor: pointer;
  }
  &__sum {
    margin-right: 10px;
  }
  &__quantity {
    margin-right: 10px;
  }
  &__basket-link {
    color: white;
    background-color: palevioletred;
    border-radius: 50%;
    height: 30px;
    width: 30px;
    text-align: center;
    vertical-align: middle;
  }
  &__basket:hover .header__basket-link {
    transform: scale(1.2);
    transition: 0.2s ease;
  }
}

.fa-shopping-basket {
  margin-right: 0;
  padding-top: 20%;
}

#menu__toggle {
  opacity: 0;
}

#menu__toggle:checked ~ .menu__btn > span {
  transform: rotate(45deg);
}
#menu__toggle:checked ~ .menu__btn > span::before {
  top: 0;
  transform: rotate(0);
}
#menu__toggle:checked ~ .menu__btn > span::after {
  top: 0;
  transform: rotate(90deg);
}
#menu__toggle:checked ~ .menu__box {
  visibility: visible;
  right: 0;
}

.menu__btn {
  display: flex;
  align-items: center;
  position: fixed;
  top: 20px;
  right: 20px;
  width: 26px;
  height: 26px;
  cursor: pointer;
  z-index: 1;
}

.menu__btn > span,
.menu__btn > span::before,
.menu__btn > span::after {
  display: block;
  position: absolute;

  width: 100%;
  height: 2px;

  background-color: white;

  transition-duration: 0.25s;
}
.menu__btn > span::before {
  content: "";
  top: -8px;
}
.menu__btn > span::after {
  content: "";
  top: 8px;
}

.menu__box {
  display: block;
  position: fixed;
  visibility: hidden;
  top: 0;
  right: -100%;
  width: 300px;
  height: 100%;
  margin: 0;
  padding: 80px 0;
  list-style: none;
  background-color: #84c7ff;
  box-shadow: 1px 0px 6px rgba(0, 0, 0, 0.2);
  transition-duration: 0.25s;
}

.menu__item {
  display: block;
  padding: 12px 24px;
  color: white;
  font-size: 20px;
  font-weight: 600;
  transition-duration: 0.25s;
}
.menu__item:hover {
  color: black;
}

.hamburger-menu {
  visibility: hidden;
  @media (max-width: 992px) {
    visibility: visible;
  }
}
</style>
