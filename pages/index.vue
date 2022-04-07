<template>
  <div>
    <h1>OCR IMAGE</h1>
    <div v-for="image in images" :key="image.id">
      <h2>{{image.name}}</h2>
      <img :src="image.url" alt="image of a black car" width="400" height="200">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      images: [
        {
          id: 1,
          name: 'car with registeration number',
          url: 'https://res.cloudinary.com/demo/image/upload/black_car.jpg',
        },
        {
          id: 2,
          name: 'car with blurred registeration number',
          url: 'https://res.cloudinary.com/demo/image/upload/e_pixelate_region:20,g_ocr_text/black_car.jpg',
      },
      ]
    }
  }
}
</script>
