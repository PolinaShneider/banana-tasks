<template>
  <div id="app">
    <h1 class="tasks-title">Задачки 🤪</h1>
    <div class="card-holder">
      <Card v-for="(task, idx) in tasks" :key="idx" :isActive="idx === activeTask" :description="task.description" :title="task.title" :cost="task.cost"/>
    </div>
  </div>
</template>

<script>
    import Card from './components/Card.vue'

    export default {
        name: 'App',
        components: {
            Card
        },
        data() {
            return {
                tasks: [
                    {title: 'Сверстать лэйаут', description: 'хедер, двухколоночный контент (70% главная часть, 30% боковое меню), футер ', cost: '2 балла'},
                    {title: 'Вставить видео с youtube', description: 'любой ролик, который тебе нравится', cost: '1 балл'},
                    {title: 'Хитрые ссылки', description: 'добавь на страницу картинку, оберни ее в ссылку, сделай так, чтобы ссылка открывалась в новом окне', cost: '2 балла'},
                    {title: 'Что по выравниванию', description: 'найди в интернете картинку про Новый год и расположи её по центру страницы (по вертикали и горизонтали)', cost: '2 балла'},
                    {title: 'Как вы помните Flexbox', description: 'за что отвечает свойство align-items: center; при flex-direction: column?', cost: '1 балл'},
                    {title: 'Создай консоль хакера', description: 'черный фон, белый текст, моноширный (monospace) шрифт, скругленные углы 8px', cost: '1 балл'},
                    {title: 'Поговорим про отступы', description: 'чем отличается padding от margin?', cost: '1 балл'},
                    {title: 'Вспомним блочную модель верстки', description: 'чем отличается элемент типа block от inline-block', cost: '1 балл'},
                    {title: 'А ты стильный?', description: 'напиши на доске три способа подключения стилей', cost: '1 балл'},
                    {title: 'Поиграем со шрифтами?', description: 'подключи на сайт шрифт Roboto Light 300 и примени его к заголовку второго уровня', cost: '1 балл'},
                    {title: 'Z-index заказывали', description: 'сверстай два квадрата и сделай так, чтобы они наезжали друг на друга', cost: '1 балл'},
                    {title: 'Безудержные танцы', description: 'исполни танец новогоднего робота (верстать ничего не надо :D)', cost: '1 балл'},
                    {title: 'Нужно больше лайков', description: 'сверстай превью фотографии вместе со счетчиком лайков, как ВКонтакте. при наведении на кнопку лайка сердечко должно окрашиваться в красный', cost: '2 балла'},
                    {title: 'Новогодний бесшовный фон', description: 'найди в интернете бесшовный фон (который можно повторять по вертикали и горизонтали, и "швы" будут незаметны) и примени его к body сайта', cost: '1 балл'},
                    {title: 'Новогодние слои', description: 'добавь на сайт картинку ёлки и при помощи работы со слоями укрась её картинками игрушек', cost: '2 балла'},
                    {title: 'Нужно больше оверлеев', description: 'сверстай затемняющий overlay, который можно наложить на любую картинку', cost: '1 балл'},
                ],
            }
        },
        computed: {
            activeTask() {
                return Math.floor(Math.random() * this.tasks.length);
            }
        }
    }
</script>

<style>
  #app {
    max-width: 1400px;
    margin: 0 auto;
  }
  .tasks-title {
    text-align: center;
  }
  .card-holder {
    display: flex;
    flex-wrap: wrap;
  }
</style>
