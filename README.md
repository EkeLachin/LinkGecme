# Link Geçme - Link redirect
Basit Link yönlendirme Sitesi.
### TR: Bu kod, bir yüklenme animasyonu gösterir ancak bu sefer dairenin içinde bir geri sayım da yapar. Geri sayım, JavaScript kullanılarak setInterval() yöntemiyle oluşturulur ve her saniye sayı 1 azaltılır. Sayfa açıldıktan sonra 5 saniye beklenir ve ardından window.location.href özelliği kullanılarak Google.com'a yönlendirilir

### EN: This code shows a loading animation, but this time also a countdown inside the circle. The countdown is created with the setInterval() method using JavaScript, and the number is decremented by 1 every second. After the page is opened, it waits for 5 seconds and then redirects to Google.com using the window.location.href attribute

# KOD - CODE

 - [ ] <!DOCTYPE html>
       
       <html lang="en">
       
       <head>
       
       <meta charset="UTF-8">
       
       <title>Yönlendiriliyorsunuz...</title>
       
       <style>
       
       /* Yüklenme animasyonu - Loading animation */
       
       .loader {
       
       border: 16px solid #f3f3f3;
       
       border-top: 16px solid #3498db;
       
       border-radius: 50%;
       
       width: 120px;
       
       height: 120px;
       
       animation: spin 2s linear infinite;
       
       margin: 100px auto;
       
       position: relative;
       
       }
       
       .countdown {
       
       font-size: 24px;
       
       position: absolute;
       
       top: 50%;
       
       left: 50%;
       
       transform: translate(-50%, -50%);
       
       }
       
       @keyframes spin {
       
       0% { transform: rotate(0deg); }
       
       100% { transform: rotate(360deg); }
       
       }
       
       </style>
       
       </head>
       
       <body>
       
       <div class="loader">
       
       <div class="countdown">5</div>
       
       </div>
       
       <script>
       
       // Geri sayım işlemi - Countdown action
       
       var countdownElement = document.querySelector(".countdown");
       
       var countdown = 5;
       
       var countdownInterval = setInterval(function() {
       
       countdown--;
       
       countdownElement.textContent = countdown;
       
       if (countdown === 0) {
       
       clearInterval(countdownInterval);
       
       }
       
       }, 1000);
       
       // Yönlendirme işlemi - Forwarding process
       
       setTimeout(function() {
       
       window.location.href = "https://www.google.com";
       
       }, 5000); // 5 saniye beklet - Wait 5 seconds
       
       </script>
       
       </body>
       
       </html>

