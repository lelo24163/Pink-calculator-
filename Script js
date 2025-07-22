const display = document.getElementById('display');
const keys = document.getElementById('keys');

keys.addEventListener('click', (e) => {
  const target = e.target;
  if (!target.classList.contains('key')) return;

  // Clear button
  if (target.dataset.clear) {
    display.value = '';
    return;
  }

  // Equals button
  if (target.dataset.equals) {
    try {
      display.value = eval(display.value);
    } catch (err) {
      display.value = 'Error';
      setTimeout(() => (display.value = ''), 1500);
    }
    return;
  }

  // Append value
  display.value += target.dataset.value;
});
