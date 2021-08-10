https://alexandervorvul.github.io/hello-world/cv
Garbage
const sliderContainer = document.querySelector('.slider-container');

const slideRight = document.querySelector('.right-slide');
const slideLeft = document.querySelector('.left-slide');

const upButton = document.querySelector('.up-button');
const downButton = document.querySelector('.down-button');

const slidesLength = document.querySelectorAll('div').length;

let activeSlideIndex = 0;

slideLeft.getElementsByClassName.top = `-${(slidesLength - 1) * 100}vh`;

//Add EventListener to the Buttons
upButton.addEventListener('click', () => changeSlide('up'));
downButton.addEventListener('click', () => changeSlide('down'));

const changeSlide = (direction) => {
    const slideHeight = sliderContainer.clientHeight;
    if (direction === 'up'){
        activeSlideIndex++;
        if (activeSlideIndex > slidesLength -1){
            activeSlideIndex = 0;
        }
    } else if (direction === 'down'){
        activeSlideIndex--;
        if (activeSlideIndex < 0){
            activeSlideIndex = slidesLength -1;
        }
    }

    slideRight.style.transform = `translateY(-${
        activeSlideIndex * sliderHeight
    }px)`;
    slideLeft.style.transform = `translateY(${
        activeSlideIndex * sliderHeight
    }px)`;
}




