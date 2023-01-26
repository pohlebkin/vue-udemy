<template>
  <div class="auth-page">
    <div class="container page">
      <div class="row">
        <div class="col-md-6 offset-md-3 col-xs-12">
          <h1 class="text-xs-center">Sign Up (регистрация)</h1>

          <p class="text-xs-center">
            <!--
            обрати внимание на эту волшебную хреновину с урлом
            смотри пояснения в уроке "7. Разметка страницы регистрации"
            -->

            <!--
            пока ссылка закомментирована
            потому что {name: 'login'} еще не прописал в @/router/index.js
            и соотвественно будет ошибка выводитсья в консоль браузера

            но в основное окно браузера ошибка не вывидится
            а вместо этого весь компонент McvRegister тупо пропадает со страницы

            у автора курса не так - ничего со страницы не пропадет

            я спрашивал GPT как можно настроить поведение при ошибках так,
            чтобы компонент не пропадал со страницы
            но GPT предлагает мне какие то трудно реализуемые способы,
            с созданием новых компонентов,
            а не просто изменение настроект проекта
            -->

            <!--
            <router-link :to="{name: 'login'}">Need an account?</router-link>
            -->
          </p>

          VALIDATION ERRORS (тут будет компонент, пока заглушка)

          <!--
          prevent запрещает дефолтное поведение формы
          -->
          <form @submit.prevent="onSubmit">
            <fieldset class="form-group">
              <input
                type="text"
                class="form-control form-control-lg"
                placeholder="username"
              />
            </fieldset>

            <fieldset class="form-group">
              <input
                type="text"
                class="form-control form-control-lg"
                placeholder="email"
              />
            </fieldset>

            <fieldset class="form-group">
              <input
                type="password"
                class="form-control form-control-lg"
                placeholder="password"
              />
            </fieldset>

            <button class="btn btn-lg btn-primary pull-xs-right">
              регистрация
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'McvRegister',
  methods: {
    onSubmit() {
      console.log('типа сабмит формы')
    },
  },
}
</script>

<style scoped></style>
