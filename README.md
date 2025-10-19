Primero creamos el proyecto, en mi caso es Ionic con Angular y NgModules. (Plantilla blank)

Una vez ya tengamos el proyecto nos vamos a: https://capacitorjs.com/docs/apis/splash-screen

Y copiamos y ejecutamos el siguiente comando en nuestro proyecto:  npm install @capacitor/splash-screen  el cual nos va a permitir trabajar con el splash screen

Luego en nuestro archivo capacitor.config.ts realizamos configuracion necesaria para usar el plugin


<img width="347" height="356" alt="image" src="https://github.com/user-attachments/assets/7b73dca0-4781-4710-a952-5769562cc110" />


Luego para poder forzar la llamada de nuestro splash screen debemos configurar el archivo app.component.ts con lo siguiente:


<img width="371" height="302" alt="image" src="https://github.com/user-attachments/assets/04dbabb1-649b-404b-b0c5-c8d1c34a8bbf" />


Despues debemos generar las plataformas android y ios (en caso de querer que funcione en ambas) con el siguiente comando:  npm i @capacitor/android @capacitor/ios
Luego generamos tanto la plataforma de android: npx cap add android
Como la de ios: npx cap add ios.

Despues de esto nos vamos a:  https://capacitorjs.com/docs/guides/splash-screens-and-icons
Y pegamos el siguiente comando que nos dan para poder generar el incono y el splash screen:  npm install @capacitor/assets
Luego hay que seguir las instrucciones de la siguiente foto


<img width="639" height="316" alt="image" src="https://github.com/user-attachments/assets/cbdc821e-2578-4ec4-af86-3507793b1115" />


Las cuales practicamente nos explican que debemos tener una carpeta llamada assets en la raiz del proyecto con las imagenes de nuestro icono y nuestro splash screen
Los nombres y tamaños tienen que ser los mismos que en la foto
Luego de crear la carpeta y las fotos entonces debemos ejecutar el siguiente comando para generar todo:  npx capacitor-assets generate

Luego ya podemos ejecutar el comando:  npx cap open android  para generar el compilado en Android Studio poder generar nuestra APK

Finalmente agregue unos cuantos permisos al AndroidManifest.xml solo en caso de que mi aplicación los requiera en un futuro.


<img width="852" height="580" alt="image" src="https://github.com/user-attachments/assets/9bf1492e-7e3e-4271-8e1f-6b9d7c51f587" />



Resultado final:
Icono personalizado

<img width="540" height="1200" alt="image" src="https://github.com/user-attachments/assets/f5a3e23f-ef0a-4e1f-a6eb-30de6ae76d7c" />


Splash Screen:


<img width="540" height="1200" alt="image" src="https://github.com/user-attachments/assets/2ee95d80-6b12-4964-8678-7d4f2de078d5" />


<img width="540" height="1200" alt="image" src="https://github.com/user-attachments/assets/d0f078dc-1040-455b-899a-18dd8b85d766" />


