<template>
  <div class="m-5">



    <div class="row">
      <div class="col">
        <h1 class="fs-3 m-3">Заполните форму:</h1>
        <form>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">Профессия</p>
            </div>
            <div class="col-9">
              <input v-model="profession" class="input-site border fs-5 p-2" type="text">
            </div>
          </div>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">Город</p>
            </div>
            <div class="col-9">
              <input v-model="city" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>



          <div class="row">
            <div class="col-3">
              <p class="fs-5">Фото</p>
            </div>
            <div class="col-9">
              <input v-model="photo" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Фалимия</p>
            </div>
            <div class="col-9">
              <input v-model="surname" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">Имя</p>
            </div>
            <div class="col-9">
              <input v-model="name" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Отчесво</p>
            </div>
            <div class="col-9">
              <input v-model="patronymic" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">Телефон</p>
            </div>
            <div class="col-9">
              <input v-model="phone" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Почта</p>
            </div>
            <div class="col-9">
              <input v-model="mail" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">Дата рождения</p>
            </div>
            <div class="col-9">
              <input v-model="bDate" class="input-site border fs-5 p-2 " type="date">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Образование</p>
            </div>
            <div class="col-9">
              <input v-model="education" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Желаемая ЗП</p>
            </div>
            <div class="col-9">
              <input v-model="money" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>

          <div class="row">
            <div class="col-3">
              <p class="fs-5">Ключевые навыки</p>
            </div>
            <div class="col-9">
              <input v-model="skills" class="input-site border fs-5 p-2 " type="text">
            </div>
          </div>


          <div class="row">
            <div class="col-3">
              <p class="fs-5">О себе</p>
            </div>
            <div class="col-9">
              <textarea  v-model="about" class="input-site border fs-5 p-2" style="height: 200px;" rows="7"></textarea>
            </div>
          </div>

        </form>
      </div>
      <div class="col">
        <h1>Ваше резюме</h1>
        <div class="border p-3">
          <p class="fs-5">Профессия</p>
          <p class="fs-5">{{ profession }}</p>
          <p class="fs-5">Город</p>
          <p class="fs-5">{{ city }}</p>
          <p class="fs-5">Фото</p>
          <p class="fs-5">{{ photo }}</p>
          <p class="fs-5">ФИО</p>
          <p class="fs-5">{{ surname }} {{name}} {{patronymic}}</p>
          <p class="fs-5">Телефон</p>
          <p class="fs-5">{{ phone }}</p>
          <p class="fs-5">Почта</p>
          <p class="fs-5">{{ mail }}</p>
          <p class="fs-5">Дата рождения</p>
          <p class="fs-5">{{ bDate }}</p>
          <p class="fs-5">Образование</p>
          <p class="fs-5">{{ education }}</p>
          <p class="fs-5">Желаемая ЗП</p>
          <p class="fs-5">{{ money }}</p>
          <p class="fs-5">Навыки</p>
          <p class="fs-5">{{ skills }}</p>
          <p class="fs-5">О себе</p>
          <p class="fs-5">{{ about }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      feet: 0,
      meter: 0,
      fToM: 3.28,
      profession: '',
      city: '',
      photo: '',
      surname: '',
      name: '',
      patronymic: '',
      phone: '',
      mail: '',
      bDate: '',
      education: '',
      money: '',
      skills: '',
      about: '',
    }
  },
  methods: {
    convertToMeter() {
      this.meter = this.feet / this.fToM;
    },
    convertToFeet() {
      this.feet = this.meter * this.fToM;
    },

  }
}
</script>

<style scoped>
.box {
  width: 900px;
}

.input-site {
  height: 35px;
  border-radius: 3px;
  width: 400px;
}
</style>