<template>
  <section id='tech-block'>
    <div class='tech-item-container'>
      <div class='tech-item'>
        <i class="fab fa-sass"></i>

        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. 
          Consequatur consequuntur commodi quis. 
          Doloremque rem nostrum ut soluta cum, a, voluptatem ipsum ipsam 
          explicabo beatae fugiat?
        </p>

        <a href='#'>Some Link </a>
      </div>

      <div class='tech-item'>
        <i class="fab fa-vuejs"></i>

        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. 
          Consequatur consequuntur commodi quis. 
          Doloremque rem nostrum ut soluta cum, a, voluptatem ipsum ipsam 
          explicabo beatae fugiat?
        </p>

        <a href='#'>Some Link </a>
      </div>
    </div>

    <button>This is a button</button>
  </section>
</template>


<script>
  export default {
    name: 'TechBlock'
  }
</script>


<style scoped lang="scss">
  @import '../colors.scss';

  #tech-block {
    width: 100%;
    padding: 3rem;
    background-color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .tech-item-container {
    width: 100%;
    min-height: 10rem;
    display: flex;
    justify-content: center;
  }

  .tech-item {
    display: flex;
    flex-direction: column;
    width: 300px;
    min-height: 10rem;
    margin: 0 5px;
    padding: 1rem;

    i{ 
      font-size: 5rem;
      color: map-get($colors, primary); 
    }
    a{ 
      text-transform: uppercase;
      color: map-get($colors, primary);
      margin-top: 1rem; 
      font-weight: bold;
      font-size: 1.3rem;
      position: relative;

      &:hover::after, &::after { transition: transform 0.2s ease}
      &::after{
        content: '';
        width: 8rem;
        height: 1px;
        position: absolute;
        bottom: -1px;
        left: 0;
        right: 0;
        background-color: map-get($colors, primary);
        transform: scaleX(0);
      }
      &:hover::after {
        transform: scaleX(1);
      }
    }
    
    p{ line-height: 2rem }
  }

  button, button:hover { 
    transition: all 0.2s ease;
    transition-property: background-color, color;
  }
  button { 
    border-radius: 0.5rem;
    margin-top: 1rem;
    padding: 1rem;
    width: 15rem;
    background-color: map-get($colors, btn-bg);
    color: map-get($colors, btn-txt);
    border: none;
    text-transform: uppercase;
    font-weight: bold;

    &:hover{
      background-color: map-get($colors, btn-hov-bg);
      color: #fff;
    }
  }

  @media screen and (max-width: 400px){
    .tech-item-container {
      display: block;
    }
    .tech-item {
      width: 100%;
      display: block;
      margin: 0 0 1rem 0;
    }

  }
</style>