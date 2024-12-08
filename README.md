let score = 0;
const target = document.getElementById('target');
const scoreDisplay = document.getElementById('score');

// Функция для перемещения мишени в случайное место
function moveTarget() {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 100);
    target.style.transform = `translate(${x}px, ${y}px)`;
}

// Обработчик клика на мишень
target.addEventListener('click', () => {
    score++;
    scoreDisplay.textContent = `Очки: ${score}`;
    moveTarget();
});

// Перемещаем мишень при загрузке страницы
moveTarget();
