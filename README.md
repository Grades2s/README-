# Hewal

<p align="center">
  <img src="https://img.shields.io/badge/Grade-<animation>?style=for-the-badge&logo=github" alt="Grade">
</p>
# Oyunu Oyna

Tıkladığınızda oyunun oynandığı bir bağlantıyı aşağıda bulabilirsiniz:

[Oyunu Oyna](javascript:(function() {
    const genislik = 800;
    const yukseklik = 600;

    const canvas = document.createElement('canvas');
    canvas.width = genislik;
    canvas.height = yukseklik;
    document.body.appendChild(canvas);

    const ctx = canvas.getContext('2d');

    const blokBoyut = 20;

    const yilan = [{
        x: genislik / 2,
        y: yukseklik / 2
    }];

    function yilanCiz() {
        ctx.clearRect(0, 0, genislik, yukseklik);
        ctx.fillStyle = 'green';
        yilan.forEach(blok => {
            ctx.fillRect(blok.x, blok.y, blokBoyut, blokBoyut);
        });
    }

    function oyunuOyna() {
        yilanCiz();

        const bas = {
            x: yilan[0].x,
            y: yilan[0].y
        };

        bas.x += blokBoyut;

        yilan.unshift(bas);

        if (yilan.length > 1) {
            yilan.pop();
        }
    }

    setInterval(oyunuOyna, 1000 / 5);
})())


<p align="center">
  <img src="https://img.shields.io/badge/Loading-<color>?style=for-the-badge&logo=github" alt="Loading">
</p>

<p align="center">
  <img src="https://media2.giphy.com/media/fLsqdVcQb6UxXOrGam/giphy.gif?cid=6c09b952agqovw810tpjmmk5osz0tmv1gt50koyz6d5y8za3&ep=v1_stickers_related&rid=giphy.gif&ct=s" alt="Loading">
</p>
