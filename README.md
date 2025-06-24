# love.html
Link Accses
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surat Cinta Untukmu</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        
        .dancing-font {
            font-family: 'Dancing Script', cursive;
        }
        
        .heart {
            position: relative;
            width: 100px;
            height: 90px;
            margin: 0 auto;
            animation: heartbeat 1.5s infinite;
        }
        
        .heart:before, .heart:after {
            position: absolute;
            content: "";
            left: 50px;
            top: 0;
            width: 50px;
            height: 80px;
            background: #ff4d6d;
            border-radius: 50px 50px 0 0;
            transform: rotate(-45deg);
            transform-origin: 0 100%;
        }
        
        .heart:after {
            left: 0;
            transform: rotate(45deg);
            transform-origin: 100% 100%;
        }
        
        @keyframes heartbeat {
            0% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
            75% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .photo-frame {
            width: 250px;
            height: 250px;
            border: 10px solid white;
            border-radius: 5px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            overflow: hidden;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .photo-frame:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }
        
        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .photo-frame:hover img {
            transform: scale(1.1);
        }
        
        .message-box {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .message-box:before {
            content: "";
            position: absolute;
            top: -10px;
            left: 20px;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.9);
            transform: rotate(45deg);
        }
        
        .login-box {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 400px;
            margin: 0 auto;
            transform: scale(0);
            opacity: 0;
            transition: all 0.5s ease;
        }
        
        .login-box.active {
            transform: scale(1);
            opacity: 1;
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .hidden {
            display: none;
        }
    </style>
</head>
<body class="flex flex-col items-center justify-center min-h-screen p-4">
    <div id="loginContainer" class="w-full max-w-md">
        <div class="login-box">
            <h2 class="text-2xl font-bold text-center text-pink-600 mb-6">Masuk Ayy</h2>
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                    Kata Sandi Nya Tanggal lahir Lengkap mu "F" besar tanpa spasi
                </label>
                <input id="password" type="password" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" placeholder="Masukkan kata sandi...">
                <p id="errorMsg" class="text-red-500 text-xs italic hidden">Kata sandi salah, coba lagi!</p>
            </div>
            <div class="flex items-center justify-center">
                <button id="loginBtn" class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline transition duration-300">
                    Buka Surat Ini
                </button>
            </div>
        </div>
    </div>

    <div id="contentContainer" class="hidden w-full">
        <div class="text-center mb-8">
            <h1 class="dancing-font text-4xl md:text-5xl font-bold text-pink-600 mb-2">Untuk Kamu Yang Tercinta</h1>
            <div class="heart mb-6"></div>
            <p class="text-gray-600 italic">Scroll ke bawah untuk membaca pesanku...</p>
        </div>

        <div class="flex flex-col md:flex-row items-center justify-center gap-8 mb-12">
            <div class="photo-frame floating">
                <img src="Foto1.JPG" alt="Foto Kita">
            </div>
            <div class="photo-frame floating" style="animation-delay: 0.5s;">
                <img src="Foto2.JPG" alt="Foto Kita">
            </div>
        </div>

        <div class="message-box mb-12">
            <p class="text-gray-800 mb-4">Halo Wanitaku, Cintaku, Manisku,</p>
            <p class="text-gray-700 mb-4">Aku Mau Nyampein sesuatu, tapi aku bukan perangkai kata yang baik hehe. Kamu adalah alasan mengapa pagi terasa lebih cerah dan malam terasa lebih indah.</p>
            <p class="text-gray-700 mb-4">Aku bersyukur bisa ketemu Kamu dalam hidupku. Senyummu adalah obat terbaik untuk hari-hariku yang lelah, dan tawamu adalah musik terindah yang pernah kudengar.</p>
            <p class="text-gray-700 mb-4">Aku minta maaf untuk Perkatanku atau sikapku yang bikin kesel kamu,aku ngga ada niat sedikitpun mau bikin kamu stres,kesel,dll. Aku berjanji akan Berubah lebih baik lagi, aku janji selalu ada untukmu, dalam suka maupun duka. Aku ingin tumbuh bersamamu, belajar bersamamu, dan membangun mimpi-mimpi kita bersama.</p>
            <p class="text-gray-700 mb-4">Terima kasih kamu sudah mau Berusaha buat Dirimu,keluargamu,dan bertahan di hubungan ini,kamu semangat terus yaa Cantik kamu pasti bisa ,Kalau duniamu sedang tidak baik" saja dan butuh bahu untuk bersandar aku akan ada disisimu ,kalau kamu perlu Tempat bercerita ceritakan sama aku, aku akan berusaha menjadi pendegar yg baik untuk setiap keluh kesahmu. Aku mencintaimu lebih dari kata-kata yang bisa diungkapkan.</p>
            <p class="text-gray-800 mt-6">Kamu inget Buat Maem ya Ayy,Sayangi Dirimu ayy jaga kesehatanmu, kamu kan janji sama aku maem teratur ayy, aku Gamau kamu sakit karna mikir terlalu berat, jangan kamu fikirin soal negara ini nda akan ikut perang nda hahaha,udah <br><span class="font-bold">Semangat ya Yoyiii</span></p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                <h3 class="text-xl font-bold text-pink-600 mb-3">Kenangan Kita</h3>
                <p class="text-gray-600">Setiap momen bersamamu adalah kenangan terindah yang akan selalu kusimpan dalam hatiku.Aku Selalu mengingat Seperti apa Bahagianya KIta Ketika Baik" Saja dan saling Bertukar Cerita</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                <h3 class="text-xl font-bold text-pink-600 mb-3">Rasa Cinta</h3>
                <p class="text-gray-600">Cintaku dan rasa Sayangku tidak akan berubah walaupun dan bagaimana pun kondisi Hubungan kita. Aku mencintaimu dengan Setulus Hati tanpa keraguan,dan mencintai semua tentangmu.bahkan Mungkin akan semakin bertumbuh nantinya</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                <h3 class="text-xl font-bold text-pink-600 mb-3">Harapan Kita</h3>
                <p class="text-gray-600">Aku berharap kita bisa terus bersama,Berjuang Mewujudkan Hubungan kita yang Bahagia Selamanya,dalam Tuhan Yesus Kristus.dan Membuktikan Ke semua Orang yang meragukan kita.</p>
            </div>
        </div>

        <div class="text-center mb-12">
            <button id="surpriseBtn" class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-6 rounded-full focus:outline-none focus:shadow-outline transition duration-300 transform hover:scale-105">
                Klik untuk Kejutan Khusus!
            </button>
        </div>

        <div id="surpriseContainer" class="hidden text-center p-8 bg-pink-50 rounded-lg mb-12">
            <h3 class="text-2xl font-bold text-pink-600 mb-4">💖 Aku Mencintaimu! 💖</h3>
            <div class="flex justify-center mb-4">
                <div class="text-4xl animate-bounce">❤️</div>
                <div class="text-4xl animate-bounce" style="animation-delay: 0.2s;">🧡</div>
                <div class="text-4xl animate-bounce" style="animation-delay: 0.4s;">💛</div>
                <div class="text-4xl animate-bounce" style="animation-delay: 0.6s;">💚</div>
                <div class="text-4xl animate-bounce" style="animation-delay: 0.8s;">💙</div>
                <div class="text-4xl animate-bounce" style="animation-delay: 1.0s;">💜</div>
            </div>
            <p class="text-gray-700">Ini adalah hari-hari terindah dalam hidupku karena aku bisa bersamamu. Terima kasih telah menjadi bagian dari hidupku.</p>
        </div>

        <footer class="text-center text-gray-500 text-sm mb-8">
            <p>Dibuat dengan ❤️ khusus untukmu</p>
            <p class="mt-2">© 2023 Surat Cinta Digital</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const password = "6Februari2002"; // Kata sandi baru
            const loginBtn = document.getElementById('loginBtn');
            const errorMsg = document.getElementById('errorMsg');
            const loginContainer = document.getElementById('loginContainer');
            const contentContainer = document.getElementById('contentContainer');
            const surpriseBtn = document.getElementById('surpriseBtn');
            const surpriseContainer = document.getElementById('surpriseContainer');
            
            // Animasi masuk untuk login box
            setTimeout(() => {
                document.querySelector('.login-box').classList.add('active');
            }, 300);
            
            // Fungsi login
            loginBtn.addEventListener('click', function() {
                const inputPassword = document.getElementById('password').value;
                
                if (inputPassword === password) {
                    loginContainer.classList.add('hidden');
                    contentContainer.classList.remove('hidden');
                    
                    // Animasi masuk untuk konten
                    contentContainer.style.opacity = 0;
                    contentContainer.style.transform = 'translateY(20px)';
                    
                    setTimeout(() => {
                        contentContainer.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                        contentContainer.style.opacity = 1;
                        contentContainer.style.transform = 'translateY(0)';
                    }, 50);
                } else {
                    errorMsg.classList.remove('hidden');
                    document.getElementById('password').classList.add('border-red-500');
                    
                    // Animasi shake untuk error
                    loginContainer.style.animation = 'shake 0.5s';
                    setTimeout(() => {
                        loginContainer.style.animation = '';
                    }, 500);
                }
            });
            
            // Event listener untuk surprise button
            surpriseBtn.addEventListener('click', function() {
                surpriseContainer.classList.toggle('hidden');
                
                if (!surpriseContainer.classList.contains('hidden')) {
                    surpriseBtn.textContent = "Sembunyikan Kejutan";
                } else {
                    surpriseBtn.textContent = "Klik untuk Kejutan Khusus!";
                }
            });
            
            // Tambahkan style untuk animasi shake
            const style = document.createElement('style');
            style.textContent = `
                @keyframes shake {
                    0%, 100% { transform: translateX(0); }
                    20%, 60% { transform: translateX(-5px); }
                    40%, 80% { transform: translateX(5px); }
                }
            `;
            document.head.appendChild(style);
            
            // Enter key untuk login
            document.getElementById('password').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    loginBtn.click();
                }
            });
        });
    </script>
</body>
</html>
