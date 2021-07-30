### Dependências importantes - Android Kotlin

URL: https://arthurgonzaga.github.io/android-dependencies/

-  ### [Architecture](#architecture)
    * [Data Binding](#data-binding)
    * [Lifecycles](#lifecycles)
    * [LiveData](#livedata)
    * [Paging](#paging)
    * [Navigation](#navigation)
    * [Room](#room)
    * [ViewModel](#viewmodel)
    * [WorkManager](#workmanager)  
<br>

* ### [Library](#library)
    * [Retrofit](#retrofit)
    * [Gson](#gson)
    * [Moshi](#moshi)
    * [Glide](#glide)
    * [Picasso](#picasso)
    * [RxJava](#rxjava)
    * [RxKotlin](#rxkotlin)
    * [RxAndroid](#rxandroid)
    * [Hilt](#hilt)
    * [Lottie](#lottie)
    * [ButterKnife](#butterknife)
    * [Mockito](#mockito)
    * [Espresso](#espresso)
    * [AndroidX Test](#AndroidX-Test)
<br>

* ### [Foundation](#foundation)
    * [AppCompat](#appcompat)
    * [Android KTX](#android-ktx)
    * [Multidex](#multidex)  
<br>



* ### [UI](#ui)
    * [Animation & transitions](#animation--transitions)
    * [Fragment](#fragment)
    * [Emoji](#emoji)
    * [Palette](#palette)  
<br>

* ### [Behavior](#behavior)
    * [Preference](#preference)
    * [Slices](#slices)  
<br>

* ### [Firebase](#firebase)
    * [Firebase Core](#firebase-core)    
    * [Realtime Database](#realtime-database)
    * [Cloud Firestore](#cloud-firestore)
    * [Authentication](#authentication)
    * [Cloud Storage](#cloud-storage)
    * [Cloud Messaging](#cloud-messaging)
    * [Cloud Functions](#cloud-functions)
    * [Crashlytics](#crashlytics)
    * [ML Kit](#ml-kit)  
<br>



---
<br>

## &#x1F4D7; **Architecture**

### **Data Binding**
Biblioteca de Data Binding Parte do Android Jetpack. A Data Binding Library é uma biblioteca de suporte que permite vincular componentes de interface do usuário em seus layouts a fontes de dados em seu aplicativo usando um formato declarativo em vez de programaticamente.

```gradle
android {
    
    dataBinding {
        enabled = true
    }
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/databinding" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/data-binding/" target="_blank">Doc</a> | <a href="https://github.com/zakaria5729/android-dependency-list/blob/master/resources/data-binding.md" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **Lifecycles**
A maioria dos componentes do aplicativo que são definidos no Android Framework têm ciclos de vida anexados a eles. Os ciclos de vida são gerenciados pelo sistema operacional ou pelo código da estrutura em execução em seu processo. Eles são fundamentais para o funcionamento do Android e seu aplicativo deve respeitá-los.

```gradle
dependencies {
    def lifecycle_version = "2.3.1"

    implementation  "androidx.lifecycle:lifecycle-extensions:$lifecycle_version"
    kapt  "androidx.lifecycle:lifecycle-compiler:$lifecycle_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/lifecycle" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/lifecycle" target="_blank">Doc</a> | <a href="https://github.com/zakaria5729/android-dependency-list/blob/master/resources/lifecycles.md" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **LiveData**
O LiveData faz parte da biblioteca Lifecycle que foi projetada para ajudá-lo a resolver desafios comuns do Android Lifecycle e tornar seus aplicativos mais fáceis de manter e testáveis. LiveData é um observável ciente do ciclo de vida. O LiveData torna mais fácil manter o que está sendo exibido na tela em sincronia com os dados.

```gradle
dependencies {
    def lifecycle_version = "2.3.1"

    // ViewModel and LiveData
    implementation "androidx.lifecycle:lifecycle-extensions:$lifecycle_version"

    // alternatively - just LiveData
    implementation "androidx.lifecycle:lifecycle-livedata:$lifecycle_version"

    // optional - ReactiveStreams support for LiveData
    implementation "androidx.lifecycle:lifecycle-reactivestreams-ktx:$lifecycle_version"

    // optional - Test helpers for LiveData
    testImplementation "androidx.arch.core:core-testing:$lifecycle_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/lifecycle" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/lifecycle" target="_blank">Doc</a> | <a href="https://github.com/zakaria5729/android-dependency-list/blob/master/resources/live-data.md" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **ViewModel**
Visão geral do ViewModel Parte do Android Jetpack. A classe ViewModel foi projetada para armazenar e gerenciar dados relacionados à IU de uma maneira consciente do ciclo de vida. A classe ViewModel permite que os dados sobrevivam às mudanças de configuração, como rotações de tela.


```gradle
dependencies {
    def lifecycle_version = "2.3.1"

    // ViewModel and LiveData
    implementation "androidx.lifecycle:lifecycle-extensions:$lifecycle_version"

    // alternatively - just ViewModel
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/lifecycle" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/lifecycle" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **Navigation**
Navigation refere-se às interações que permitem aos usuários navegar entre, para dentro e para fora das diferentes partes do conteúdo em seu aplicativo. O componente de Navigation do Android Jetpack ajuda a implementar a navegação, desde simples cliques em botões até padrões mais complexos, como barras de aplicativos e gaveta de navegação.

```gradle
dependencies {
    def nav_version = "2.3.5"

    implementation "androidx.navigation:navigation-fragment-ktx:$nav_version"
    implementation "androidx.navigation:navigation-ui-ktx:$nav_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/navigation" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/navigation.html" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **Paging**
A biblioteca de Paging faz parte do Android Jetpack. A Biblioteca de Paging ajuda a carregar e exibir pequenos blocos de dados por vez.

```gradle
dependencies {
    def paging_version = "3.0.1"

    implementation "androidx.paging:paging-runtime-ktx:$paging_version"

    // alternatively - without Android dependencies for testing
    testImplementation "androidx.paging:paging-common-ktx:$paging_version"

    // optional - RxJava support
    implementation "androidx.paging:paging-rxjava2-ktx:$paging_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/paging" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/paging/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **Room**
Biblioteca de persistência de Room Parte do Android Jetpack. A biblioteca de persistência da Room oferece uma camada de abstração sobre o SQLite para permitir um acesso mais robusto ao banco de dados, aproveitando todo o poder do SQLite. A biblioteca ajuda a criar um cache dos dados do seu aplicativo em um dispositivo que está executando o seu aplicativo.

```gradle
dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    kapt "androidx.room:room-compiler:$room_version"

    // optional - Kotlin Extensions and Coroutines support for Room
    implementation "androidx.room:room-ktx:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // Test helpers
    testImplementation "androidx.room:room-testing:$room_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/room" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/room" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

### **WorkManager**
WorkManager é uma biblioteca Android Jetpack que executa um trabalho em segundo plano adiável e garantido quando as restrições do trabalho são satisfeitas. WorkManager é a prática recomendada atual para muitos tipos de trabalho em segundo plano.

```gradle
dependencies {
    def work_version = "2.5.0"

    implementation "androidx.work:work-runtime-ktx:$work_version"

    // optional - Test helpers
    androidTestImplementation "androidx.work:work-testing:$work_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/work" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/architecture/workmanager" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#architecture">↥ Back to top</a> </b>
</div>

---
<br>

## &#x1F4D7; **Library**

### **Retrofit**
Retrofit é um cliente REST para Android e Java da Square. Isso torna relativamente fácil recuperar e fazer upload de JSON (ou outros dados estruturados) por meio de um serviço da web baseado em REST. No Retrofit você configura qual conversor será utilizado para a serialização dos dados.

```gradle
dependencies {
    implementation 'com.squareup.retrofit2:retrofit:2.9.0'
}
```

<a href="http://square.github.io/retrofit/#download" target="_blank">Release</a> | <a href="http://square.github.io/retrofit/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Gson**
Gson é uma biblioteca Java que pode ser usada para converter objetos Java em sua representação JSON. Ele também pode ser usado para converter uma string JSON em um objeto Java equivalente. Gson pode trabalhar com objetos Java arbitrários, incluindo objetos pré-existentes dos quais você não possui o código-fonte.

```gradle
dependencies {
    implementation 'com.squareup.retrofit2:converter-gson:2.8.7'
}
```

<a href="http://square.github.io/retrofit/#resadapter-configuration" target="_blank">Release</a> | <a href="http://square.github.io/retrofit/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Glide**
Glide é uma biblioteca Image Loader para Android desenvolvida pela bumptech e é uma biblioteca recomendada pelo Google. Ele tem sido usado em muitos projetos de código aberto do Google, incluindo o aplicativo oficial do Google I / O 2014. Ele fornece suporte a GIF animado e controla o carregamento / armazenamento de imagens.

```gradle
dependencies {
    kapt "android.arch.lifecycle:compiler:2.3.1"
    kapt 'com.github.bumptech.glide:compiler:4.11.0'
}
```

<a href="https://bumptech.github.io/glide/doc/configuration.html" target="_blank">Release</a> | <a href="https://bumptech.github.io/glide/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Picasso**
Picasso é uma biblioteca de imagens para Android. É criado e mantido pela Square e atende ao carregamento e processamento de imagens. Ele simplifica o processo de exibição de imagens de locais externos.

```gradle
dependencies {
    implementation 'com.squareup.picasso:picasso:2.71828'
}
```

<a href="https://square.github.io/picasso/#download" target="_blank">Release</a> | <a href="https://square.github.io/picasso/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **RxJava**
Se você é um desenvolvedor Android, provavelmente já ouviu falar do RxJava. É uma das bibliotecas mais discutidas para habilitar a Programação Reativa no desenvolvimento do Android. É apresentado como a estrutura de referência para simplificar as tarefas simultâneas / assíncronas inerentes à programação móvel.

```gradle
dependencies {
    implementation 'io.reactivex.rxjava2:rxjava:2.2.0'
}
```

<a href="https://github.com/ReactiveX/RxJava/wiki/Getting-Started" target="_blank">Release</a> | <a href="https://github.com/ReactiveX/RxJava/wiki/How-To-Use-RxJava" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>  

---
<br>


### **RxKotlin**
RxKotlin / RxJava fornece uma maneira fácil e eficiente de lidar com o fluxo assíncrono de dados em programas executados na Java Virtual Machine (JVM). Alguns exemplos de eventos assíncronos podem ser Solicitações de Rede, Eventos de Entrada de Toque, etc. Rx em RxKotlin significa Extensões Reativas.

```gradle
dependencies {
    implementation 'io.reactivex.rxjava2:rxkotlin:x.y.z'
}
```

```gradle
// Building with JitPack
repositories {
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'com.github.ReactiveX:RxKotlin:2.x-SNAPSHOT'
}
```

<a href="https://github.com/ReactiveX/RxKotlin/releases" target="_blank">Release</a> | <a href="https://github.com/ReactiveX/RxKotlin" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>  

---
<br>

### **RxAndroid**
É uma das bibliotecas mais discutidas para habilitar a Programação Reativa no desenvolvimento do Android. É apresentado como a estrutura de referência para simplificar as tarefas simultâneas / assíncronas inerentes à programação móvel.

```gradle
dependencies {
    implementation 'io.reactivex.rxjava2:rxandroid:2.1.1'
}
```

<a href="https://github.com/ReactiveX/RxAndroid/wiki" target="_blank">Release</a> | <a href="https://github.com/ReactiveX/RxAndroid/wiki" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Hilt**
O Hilt é uma biblioteca de injeção de dependência para Android que reduz a injeção manual de código de texto clichê no projeto. O Hilt foi criado com base na conhecida biblioteca de DI Dagger para aproveitar a precisão do tempo de compilação, o desempenho no tempo de execução, a escalonabilidade e o suporte do Android Studio fornecido pelo Dagger.

#### build.gradle (project)
```gradle
buildscript {

   ext {
        ...
        hilt_version = "2.37"
    }
    
    dependencies {
        ...
        classpath "com.google.dagger:hilt-android-gradle-plugin:$hilt_version"
    }
}
```

#### build.gradle (app)
```gradle
apply plugin: 'kotlin-kapt'
apply plugin: 'dagger.hilt.android.plugin'

android {
    ...
}

dependencies {
    implementation "com.google.dagger:hilt-android:$hilt_version"
    kapt "com.google.dagger:hilt-android-compiler:$hilt_version"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/hilt" target="_blank">Release</a> | <a href="https://developer.android.com/training/dependency-injection/hilt-android" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Lottie**
Lottie é uma biblioteca para Android, iOS, Web e Windows que analisa animações do Adobe After Effects exportadas como json com Bodymovin e as renderiza nativamente no celular e na web.

```gradle
dependencies {
    implementation "com.airbnb.android:lottie:2.8.0"
}
```

<a href="https://airbnb.io/lottie/#/android" target="_blank">Release</a> | <a href="https://airbnb.io/lottie/#/android" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Mockito**
Mockito é um framework mock popular que pode ser usado em conjunto com JUnit. O Mockito permite criar e configurar objetos fictícios. O uso do Mockito simplifica significativamente o desenvolvimento de testes para classes com dependências externas.

```gradle
dependencies {
    testImplementation 'org.mockito:mockito-inline:2.8.47'
}
```

<a href="https://site.mockito.org/#how" target="_blank">Release</a> | <a href="https://site.mockito.org/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

### **Espresso**
A estrutura de teste do Espresso. O Espresso é uma estrutura de teste para Android que torna mais fácil escrever testes de interface de usuário confiáveis. A estrutura também garante que sua atividade seja iniciada antes da execução dos testes.

```gradle
dependencies {
    androidTestImplementation 'com.android.support.test.espresso:espresso-core:3.0.2'
    androidTestImplementation 'com.android.support.test:runner:1.0.2'
    androidTestImplementation 'com.android.support.test:rules:1.0.2'
}
```

<a href="https://developer.android.com/training/testing/set-up-project" target="_blank">Release</a> | <a href="https://developer.android.com/training/testing/espresso/setup" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>


### **AndroidX Test**
AndroidX Test é uma coleção de bibliotecas para teste. Inclui classes e métodos que fornecem versões de componentes como Aplicativos e Atividades, destinados a testes. Como exemplo, este código que você escreveu é um exemplo de uma função de teste AndroidX para obter um contexto de aplicativo.

```gradle
dependencies {
      // Core library
      androidTestImplementation 'androidx.test:core:1.0.0'
      
      // Test livedata
      testImplementation "androidx.arch.core:core-testing:$archTestingVersion"

      // AndroidJUnitRunner and JUnit Rules
      androidTestImplementation 'androidx.test:runner:1.1.0'
      androidTestImplementation 'androidx.test:rules:1.1.0'

      // Assertions
      androidTestImplementation 'androidx.test.ext:junit:1.0.0'
      androidTestImplementation 'androidx.test.ext:truth:1.0.0'
      androidTestImplementation 'com.google.truth:truth:1.1.3'

      // Espresso dependencies
      androidTestImplementation 'androidx.test.espresso:espresso-core:3.1.0'
      androidTestImplementation 'androidx.test.espresso:espresso-contrib:3.1.0'
      androidTestImplementation 'androidx.test.espresso:espresso-intents:3.1.0'
      androidTestImplementation 'androidx.test.espresso:espresso-accessibility:3.1.0'
      androidTestImplementation 'androidx.test.espresso:espresso-web:3.1.0'
      androidTestImplementation 'androidx.test.espresso.idling:idling-concurrent:3.1.0'
      
      // Robolectric
       testImplementation "org.robolectric:robolectric:4.4"
}
```
###### app/build.gradle
```gradle
testOptions.unitTests { includeAndroidResources = true }
```

<a href="https://developer.android.com/jetpack/androidx/releases/test" target="_blank">Release</a> | <a href="https://developer.android.com/training/testing/set-up-project" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#library">↥ Back to top</a> </b>
</div>

---
<br>

## &#x1F4D7; **Behavior**

### **Preference**
Preference components and attributes Part of Android Jetpack. This topic describes some of the most commonly-used Preference components and attributes used when building a settings screen.

```gradle
dependencies {
    implementation 'androidx.preference:preference-ktx:1.0.0'
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/preference" target="_blank">Release</a> | <a href="https://developer.android.com/guide/topics/ui/settings" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#behavior">↥ Back to top</a> </b>
</div>

---
<br>

### **Slices**
Slices display rich content and actions on components, appearing as part of search results in the Google search app. They can display a variety of content types, such as text, images, and actions.

```gradle
dependencies {
    implementation 'androidx.slice:slice-builders-ktx:1.0.0-alpha3'
    implementation 'androidx.annotation:annotation:1.0.0-alpha3'
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/slice" target="_blank">Release</a> | <a href="https://developer.android.com/guide/slices" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#behavior">↥ Back to top</a> </b>
</div>

---
<br>

## &#x1F4D7; **Foundation**

### **AppCompat**
AppCompat library Part of Android Jetpack. AppCompat is a set of support libraries which can be used to make the apps developed with newer versions work with older versions. Note:The appcompat library has migrated into the AndroidX library, which is an Android Jetpack component.

```gradle
dependencies {
    implementation "androidx.appcompat:appcompat:1.0.2"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/appcompat" target="_blank">Release</a> | <a href="https://developer.android.com/topic/libraries/support-library/packages.html#v7-appcompat" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#foundation">↥ Back to top</a> </b>
</div>

---
<br>

### **Android KTX**
Android KTX is a set of Kotlin extensions that is part of the Android Jetpack family. Android KTX does not add any new features to the existing Android APIs.

```gradle
dependencies {
    implementation "implementation 'androidx.core:core-ktx:1.0.1"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/core" target="_blank">Release</a> | <a href="https://developer.android.com/kotlin/ktx.html" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#foundation">↥ Back to top</a> </b>
</div>

---
<br>

### **Multidex**
Dex is short for Dalvik Executable, which is what Google's virtual machine processor (Dalvik) uses to handle Android Applications. MultiDex integration in Android Studio allows Android Developers the ability to compile and execute a code-base with over 65,536 methods!

__Note:__ Therefore, if your minSdkVersion is 21 or higher, you do not need the multidex support library.

```gradle
dependencies {
    implementation "com.android.support:multidex:1.0.3"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/multidex" target="_blank">Release</a> | <a href="https://developer.android.com/studio/build/multidex.html" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#foundation">↥ Back to top</a> </b>
</div>

---
<br>

## &#x1F4D7; **UI**

### **Emoji**
Google emoji images are used on stock Android devices (such as Pixel phones), Gmail Web Interface, Google Hangouts, and ChromeOS. Apps such as WhatsApp and Facebook use their own emoji images, while Signal and Telegram for Android use Apple emoji images.

```gradle
dependencies {
    implementation "com.android.support:support-emoji:28.0.0"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/emoji" target="_blank">Release</a> | <a href="https://developer.android.com/guide/topics/ui/look-and-feel/emoji-compat" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#ui">↥ Back to top</a> </b>
</div>

---
<br>

### **Fragment**
Android Fragments is a "reusable self contained portions of a user interface" in an Android Activity used for creating dynamic and flexible user interface.Fragments has it's own life cycle but it always be embedded with an activity so that the fragments life cycle is directly affected by the host activity's life cycle. 

```gradle
dependencies {
    implementation "androidx.fragment:fragment-ktx:1.1.0-alpha06"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/fragment" target="_blank">Release</a> | <a href="https://developer.android.com/guide/components/fragments" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#ui">↥ Back to top</a> </b>
</div>

---
<br>

### **Animation & transitions**
Android's Animation & transition framework allows you to animate all kinds of motion in your UI by simply providing the starting layout and the ending layout.

```gradle
dependencies {
    implementation "androidx.dynamicanimation:dynamicanimation-ktx:1.0.0-alpha02" //dynamic animation
    implementation "androidx.transition:transition:1.1.0-beta01"
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/fragment" target="_blank">Release</a> | <a href="https://developer.android.com/guide/components/fragments" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#ui">↥ Back to top</a> </b>
</div>

---
<br>

### **Palette**
Palette is a new API for Android that allows you to extract and make use of colors in an image. It also has a support library in order for older versions of Android to make use of Palette. All you need is an image bitmap and the Palette library, and you're good to go.

__Note:__ To use the palette library, you have to use the Android Support Library to version __24.0.0 or higher__

```gradle
dependencies {
    implementation 'com.android.support:palette-v7:28.0.0'
}
```

<a href="https://developer.android.com/jetpack/androidx/releases/palette" target="_blank">Release</a> | <a href="https://developer.android.com/training/material/palette-colors" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#ui">↥ Back to top</a> </b>
</div>

---
<br>

## &#x1F4D7; **Firebase**

### **Firebase Core**
Firebase is a mobile platform that helps you quickly develop high-quality apps, grow your user base, and earn more money. Firebase is made up of complementary features that you can mix-and-match to fit your needs, with Google Analytics for Firebase at the core.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-core:16.0.8"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Realtime Database**
The Firebase Realtime Database is a cloud-hosted database. When you build cross-platform apps with our iOS, Android, and JavaScript SDKs, all of your clients share one Realtime Database instance and automatically receive updates with the newest data.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-database:16.1.0"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/database/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Cloud Firestore**
Use our flexible, scalable NoSQL cloud database to store and sync data for client- and server-side development. Cloud Firestore is a flexible, scalable database for mobile, web, and server development from Firebase and Google Cloud Platform.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-firestore:18.2.0"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/firestore/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Authentication**
Firebase Authentication provides backend services, easy-to-use SDKs, and ready-made UI libraries to authenticate users to your app. It supports authentication using passwords, phone numbers, popular federated identity providers like Google, Facebook and Twitter, and more.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-auth:16.2.1"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/auth/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Cloud Storage**
Firebase Cloud Storage is a powerful, simple, and cost-effective object storage service. It includes Google security to file uploads and downloads for your Firebase apps. Cloud Storage allows us to store images, audio, video, or other user-generated content.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-storage:16.1.0"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/storage/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Cloud Messaging**
Firebase Cloud Messaging (FCM) is a cross-platform messaging solution that lets you reliably deliver messages at no cost. Using FCM, you can notify a client app that new email or other data is available to sync.

```gradle
dependencies {
    implementation "com.google.firebase:firebase-messaging:17.6.0"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/cloud-messaging/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Cloud Functions**
Cloud Functions for Firebase lets you create functions that are triggered by Firebase products, such as changes to data in the Realtime Database, uploads to Cloud Storage, new user sign ups via Authentication, and conversion events in Analytics.

```gradle
dependencies {
    implementation "https://firebase.google.com/docs/functions/"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/functions/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **Crashlytics**
Firebase Crashlytics is a lightweight, realtime crash reporter that helps you track, prioritise, and fix stability issues to improve your app quality.

```gradle
dependencies {
    implementation "com.crashlytics.sdk.android:crashlytics:2.9.9"
    implementation "com.google.firebase:firebase-crash:16.2.1" //Crash Reporting
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/crashlytics/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>

### **ML Kit**
Firebase ML Kit was introduced to us at Google I/O '18. It is a mobile SDK that enables Android and iOS app developers to have advanced machine learning capabilities into their apps with ease.

```gradle
dependencies {
    //Vision APIs
    implementation "com.google.firebase:firebase-ml-vision:19.0.3"

    //Image Labeling Model
    implementation "com.google.firebase:firebase-ml-vision-image-label-model:17.0.2"

    //Face Detection Model
    implementation "com.google.firebase:firebase-ml-vision-face-model:17.0.2"

    //Natural Language APIs
    implementation "com.google.firebase:firebase-ml-natural-language:18.2.0"

    //Language Identification Model
    implementation "com.google.firebase:firebase-ml-natural-language-language-id-model:18.0.3"

    //Smart Reply Model
    implementation "com.google.firebase:firebase-ml-natural-language-smart-reply-model:18.0.0"

    //Custom Model APIs
    implementation "com.google.firebase:firebase-ml-model-interpreter:18.0.0"
}
```

<a href="https://firebase.google.com/support/release-notes/android" target="_blank">Release</a> | <a href="https://firebase.google.com/docs/ml-kit/" target="_blank">Doc</a> | <a href="" target="_blank">Resources</a>

<div align="right">
    <b> <a href="#firebase">↥ Back to top</a> </b>
</div>

---
<br>
