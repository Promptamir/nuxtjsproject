<template>
  <div class="flex flex-col md:items-start items-center login">
    <div class="title-box">
      <span></span>
      login now
    </div>
    <div class="relative max-w-max">
      <div class="flex flex-col md:items-start items-center relative md:items-start items-center z-10">
        <h2 class="section-title-1">
          welcome back to your
        </h2>
        <h3 class="section-title-2">
          beauty & health family
        </h3>
      </div>
      <img src="~/assets/images/img/whyusTextBg.png" class="w-full absolute bottom-0" style="border-radius: 100px"
           alt="">
    </div>
    <p class="text-sm md:text-base login-desc mt-3 md:mt-5 md:text-left text-center">
      Log in to your account quickly, enjoy our best services for your journey.
    </p>
  </div>
</template>

<script>
import LSTabs from "~/components/pages/ls/LSTabs";
import LoginWithGA from "~/components/pages/ls/LoginWithGA";
import TextInput from "~/components/elements/TextInput";
import Button from "~/components/elements/Button";

export default {
  components: {Button, TextInput, LoginWithGA, LSTabs},
  methods: {
    changedTab(id) {
      this.$emit('changed', id)
    }
  }
}
</script>

<style scoped lang="scss">
.login {
  padding-top: 26px;

  .section-title-1 {
    font-size: 20px;
  }

  .section-title-2 {
    font-size: 40px;
  }

  &-desc {
    color: #565656;
  }
}

@media screen and (max-width: 1164px) {
  .login {

    .section-title-2 {
      font-size: 34px;
    }
  }
}

@media screen and (max-width: 1023px) {
  .login {
    padding-top: 0;
  }
}

@media screen and (max-width: 767px) {
  .login {
    .section-title-1 {
      font-size: 13px;
    }

    .section-title-2 {
      font-size: 22px;
    }
  }
}
</style>
