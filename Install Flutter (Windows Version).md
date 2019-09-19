<h1>Cara Instal Flutter untuk Komputer Spesifikasi Ringan (Windows Version)</h1>
  <h2>Topik</h2>
    <ul>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#download-sdk-flutter">Download SDK Flutter</a></li>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#download-basic-android-command-line-tools">Download Basic Android Command Line Tools</a></li>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#download-jdk8u212-b03">Download jdk8u212-b03</a></li>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#membuat-direktori-baru">Membuat Direktori Baru</a></li>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#ekstrak-dan-moving-file">Ekstrak dan Moving File</a></li>
      <li><a href="https://github.com/Jufrenbarasa/Mobile-Programming/blob/master/Install%20Flutter%20(Windows%20Version).md#set-environment-variable-dan-path">Set Environment Variable dan Path</a></li>
    </ul>

  <h2>Persiapan</h2>
    <p>Sebelum instalasi, ada beberapa komponen yang perlu Anda siapkan. Berikut langkah-langkahnya.</p>
    <h3>Download SDK Flutter</h3>
    <p>
    Silahkan Anda kunjungi <a href="https://flutter.dev/docs/development/tools/sdk/releases">website</a> Flutter untuk mendownload file sdk. Disana Anda bisa memilih chanel apa yang Anda butuhkan, seperti: Stable, Beta, Dev atau Master Chanel. Di tutorial ini menggunakan sdk Flutter, Stable Chanel.
    </p>

   <h3>Download Basic Android Command Line Tools</h3>
    <p>
  Jika Anda tidak membutuhkan Android Studio, Anda bisa mengunjungi <a href="https://developer.android.com/studio/#command-tools">website</a> ini untuk mendownload basic Android.
    </p>

   <h3>Download jdk8u212-b03</h3>
     <p>
      Download file tersebut di <a href="https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/tag/jdk8u212-b03">website</a> ini.
    </p>

   <h3>Membuat Direktori Baru</h3>
    <p>Jika langkah-langkah di atas sudah Anda selesaikan, maka selanjutnya adalah membuat direktori baru dengan nama “Android” di dalam “C:\”.</p>

   <h3>Ekstrak dan Moving File</h3>
    <p>
    Cari file yang sudah Anda download kemudian ekstrak lalu pindahkan file tersebut ke direktori Android.<br>
    <b>Catatan: rename folder “jdk8u212-b03” dengan openjdk.</b><br>
    Path: C:\Android
    </p>

   <h3>Set Environment Variable dan Path</h3>
    <p>
    Buka command prompt di windows Anda, run as administrator. Kemudian copy and paste command per baris kemudian enter untuk men-set variable dan path.
    <ul>
      <li>setx JAVA_HOME “C:\Android\openjdk”</li>
      <li>setx ANDROID_HOME “C:\Android”</li>
      <li>setx ANDROID_SDK_ROOT “C:\Android\tools”</li>
      <li>setx path “%path%;”C:\Android\sdk;C:\Android\tools\bin;C:\Android\flutter\bin”</li>
    </ul>
    
   Kemudian di command prompt arahkan ke path berikut:
   C:/Android/tools/bin 
   </p>
Lalu jalankan copy and paste per baris dan jalankan perintah tersebut.
<ul>
  <li>sdkmanager “system-images;android-28;default;x86_64”</li>
  <li>sdkmanager “platform-tools”</li>
  <li>sdkmanager “build-tools;28.0.3”</li>
  <li>sdkmanager “platforms;android-28”</li>
</ul>
Update Android SDK (Last Version)
Untuk sdk, Flutter selalu memerlukan Android SDK yang terbaru. jadi silahkan update sdk dengan command di bawah ini:
sdkmanager —-update

Kemudian jangan lupa untuk accept licenses-nya:
flutter doctor --android-licenses

Selanjutnya install Visual Studio Code beserta ekstension flutter dan dart.
Jika semuanya sudah selesai, silahkan Anda buka C:\Android\Flutter\flutter_console.bat

Kemudian jalankan perintah flutter doctor, maka hasilnya seperti gambar berikut.
</p>

<p>
Step terakhir adalah buat project di VsCode dengan klik F1 dan mengetikan Flutter: New Project setelah project selesai di load, klik F5 untuk mendeploy ke android device teman-teman. dan hasilnya seperti gambar dibawah ini
</p>
