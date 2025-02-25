
document.addEventListener("DOMContentLoaded", function () {
    let wishlist = JSON.parse(localStorage.getItem('wishlist')) || [];

    document.querySelectorAll('.add-to-wishlist').forEach(button => {
        let productId = button.getAttribute('data-product-id');

        // Оновлення вигляду кнопки, якщо товар у списку бажань
        if (wishlist.includes(productId)) {
            button.classList.add('added');
            button.textContent = "✔ У списку бажань";
        }

        button.addEventListener('click', function () {
            if (!wishlist.includes(productId)) {
                wishlist.push(productId);
                button.classList.add('added');
                button.textContent = "✔ У списку бажань";
            } else {
                wishlist = wishlist.filter(id => id !== productId);
                button.classList.remove('added');
                button.textContent = "❤️ Додати у список бажань";
            }
            localStorage.setItem('wishlist', JSON.stringify(wishlist));
        });
    });
});
