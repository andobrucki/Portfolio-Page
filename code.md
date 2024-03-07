@use "variables" as *;
@use "header" as *;
@use "footer" as *;
@use "placeholder" as *;

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  font-family: "Open Sans", sans-serif;
}

// Body Style

body {
  background-color: $primary-color;
  height: 100vh;
}

// Main Style

main {
  width: 90%;
  height: 80vh;
  margin: 5rem auto;
  border: 2px solid yellow;
}

.main__hero {
  h2 {
    font-family: "Namdhinggo", serif;
    font-size: 2rem;
    color: $neutral-color-dark;
    text-align: right;
  }
}

.main__hero-works {
  // display: grid;
  gap: 1rem 1rem;
  border: black solid 1px;
  // grid-template-columns: repeat (4, 25%);
  // grid-template-rows: repeat(4, 1fr);
  // grid-template-areas:
  //   "a a a a"
  //   "b b b b"
  //   "c c c c"
  //   "d d d d";
}

.hero-works-1__container {
  position: relative;
  width: 100%;
  border: 2px yellow solid;
}

.hero-works__img-1 {
  border: blue 2px solid;
  display: block;
  width: 100%;
  height: auto;
}

.img-1__overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: $secondary-color;
}

.hero-works-1__container:hover .img-1__overlay {
  opacity: 1;
}

.img-1__overlay-text {
  color: $neutral-color-light;
  font-size: 1rem;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}

@media screen and (min-width: 800px) {
  .main__impressum {
    background-color: red;
    // display: grid;
    // grid-template-columns: 50% 50%;
    // grid-template-rows: repeat(10, 1fr);

    .impressum-1 {
      grid-column: 1 / 2;
    }

    .impressum-2 {
      grid-column: 2 / 3;
    }
  }
}
