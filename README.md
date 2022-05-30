# GOIT-MARAFON
Summary

// Удалить CSS-класс square-transition
const square = document.querySelector('.features');
square.classList.remove('square-transition');

// Добавить наблюдение за появлением элемента
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      square.classList.add('square-transition');
      return;
    }
    square.classList.remove('square-transition');
  });
});
observer.observe(document.querySelector('.features'));
