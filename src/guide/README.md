# Introducción
Nueva versión de la aplicación GanaMóvil

## Descripción
Proyecto de la nueva versión de GanaMóvil bajo la tendencia Open Source implementado con la biblioteca React Native v0.69.

[![Build Status](https://camo.githubusercontent.com/581876c6737fdf87aa502305c12f83af6fc0f1c9fdb4c40e359582d688c10c31/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f72656163742d6e61746976653f636f6c6f723d627269676874677265656e266c6162656c3d6e706d2532307061636b616765)](https://www.npmjs.com/package/react-native)

React Native trae el marco de interfaz de usuario declarativo de [**React**][r] para iOS y Android. Con React Native, usa controles de interfaz de usuario nativos y tiene acceso completo a la plataforma nativa.
## Entorno
### **Configuración del entorno de desarrollo (Windows)**

Necesitará Node, la interfaz de línea de comandos de React Native, un JDK y Android Studio.

| Software       | Versión  |
| -------------- | -------- |
| NodeJS         | 16.4     |
| OpenJDK        | 11       |
| Android Studio | 2021.2.1 |

 Recomendamos instalar el JDK a través de Chocolatey , un popular administrador de paquetes para Windows.

#### **Instalación NodeJS**

Descargue el instalador en su versión estable(LTS). Asegúrese de que sea Node 14 o posterior, y prosiga con la instalación típica de Windows.

 De preferencia no instalar el administrador de Software **Chocolatey**.

#### **Instalación Android Studio**

Descargue **[Android Studio](https://developer.android.com/studio/index.html)** de preferencia en su última o penúltima versión. Mientras esté en el asistente de instalación de Android Studio, asegúrese de que las casillas junto a todos los siguientes elementos estén marcadas:

- ```Android SDK```
- ```Android SDK Platform```
- ```Android Virtual Device```
- Si aún no está utilizando Hyper-V: Performance (Intel ® HAXM)( Consulte aquí para AMD o Hyper-V )

Luego, haga clic en **Siguiente** para instalar todos estos componentes.

> Android Studio instala el SDK de Android más reciente de forma predeterminada. Sin embargo, la creación de una aplicación React Native con código nativo requiere el Android 11 (R)SDK en particular. Se pueden instalar SDK de Android adicionales a través del SDK Manager en Android Studio.

##### **Android 11 SDK**

1.Para instalar abra Android Studio, haga clic en el botón "Configurar" y seleccione "Administrador de SDK".

> SDK Manager también se puede encontrar en el cuadro de diálogo "Preferencias" de Android Studio, en ``Apariencia y comportamiento`` → ``Configuración del sistema`` → ``SDK de Android``.

2.Seleccione la pestaña **Plataformas de SDK** dentro del Administrador de SDK, luego marque la casilla junto a **Mostrar detalles del paquete** en la esquina inferior derecha.

3.Busque y expanda el grupo Android 11 (R), luego asegúrese de que los siguientes elementos estén marcados:

   1. ``Android SDK Platform 30``

   2. ```Intel x86 Atom_64 System Image``` o ```Google APIs Intel x86 Atom System Image.```

4.A continuación, seleccione la pestaña ``Herramientas SDK`` y marque la casilla junto a ``Mostrar detalles del paquete``.

5.Busque y expanda la entrada ```Android SDK Build-Tools```, luego asegúrese de que ```30.0.2``` esté seleccionada.

Finalmente, haga clic en "Aplicar" para descargar e instalar el SDK de Android y las herramientas de compilación relacionadas.

##### **Variables de Entorno Android Studio**

1. Abra el Panel de control de Windows.

2. Haga clic en Cuentas de usuario, luego haga clic en Cuentas de usuario nuevamente.

3. Haga clic en Cambiar mis variables de entorno.

4. Haga clic en Nuevo... para crear una nueva variable de usuario ```ANDROID_HOME``` que apunte a la ruta a su SDK de Android:

   ```sh
   %LOCALAPPDATA%\Android\Sdk
   ```

##### **Herramientas de plataforma a Path**

1. Abra el Panel de control de Windows.

2. Haga clic en Cuentas de usuario, luego haga clic en Cuentas de usuario nuevamente.

3. Haga clic en Cambiar mis variables de entorno.

4. Seleccione la variable ``Path``.

5. Haga clic en Editar.

6. Haga clic en Nuevo y agregue la ruta a las herramientas de la plataforma a la lista.

7. La ubicación predeterminada para esta carpeta es:

     ```sh
     %LOCALAPPDATA%\Android\Sdk\platform-tools
     ```

##### **Preparando el dispositivo Android**

##### **Usar un dispositivo físico**

Si tiene un dispositivo Android físico, puede usarlo para el desarrollo en lugar de un AVD conectándolo a su computadora con un cable USB.

 Asegúrese que el dispositivo que usara tenga habilitado la opción ```Depuración USB``` y la ```Instalación vía usb``` en caso de que su dispositivo lo requiera.

##### **Usar un dispositivo virtual**

Si instaló Android Studio recientemente, es probable que deba crear un nuevo AVD . Seleccione **Crear dispositivo virtual...**, luego elija cualquier teléfono de la lista y haga clic en "Siguiente", luego seleccione la imagen Q API Nivel 30.

 Si no tiene HAXM instalado, haga clic en **Instalar HAXM** o siga estas instrucciones para configurarlo, luego regrese al Administrador de AVD.

#### **(Opcional) Instalación de Chocolatey (Windows)**

1. Asegúrese de estar utilizando un Powerhell administrativo.

2. Ejecute el siguiente comando:  **```Get-ExecutionPolicy```**. Si la shell regresa como respuesta: **```Restricted```**, ejecute: **```Set-ExecutionPolicy AllSigned```**

3. Ahora ejecute la siguiente sentencia: **``Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))``**

4. Espere unos segundos para que se complete el comando.

5. Si no ve ningún error, ¡está listo para usar Chocolatey!.

#### **Instalación JDK 11 con Chocolatey**

Abra un Símbolo del sistema de administrador (haga clic con el botón derecho en Símbolo del sistema y seleccione **Ejecutar como administrador**), luego ejecute el siguiente comando:

```sh
choco install -y openjdk11
```
## Accesos
Se necesitara tener acceso al repositorio del proyecto **FRONTEND-REACT-NATIVE** alojado en *Gitlab*.
`https://gitlab.bg.com.bo/desarrollo/bga/app-movil/ganamovil/frontend-react-native` <br>
Para solicitar la respectiva accesibilidad al proyecto puede hacer [click aquí.](https://forms.office.com/Pages/ResponsePage.aspx?id=Py2m7g8taUSU6KBa09Nzk93GFqunBnxOhQBvTMZXS3pUODRMT0JSNTBEREczVEhGQlBDM1YyQUdDTy4u).

## **Primeros pasos**

Abra un símbolo del isstema, realiza la clonación del proyecto y navega al proyecto.

```sh
git clone https://gitlab.bg.com.bo/desarrollo/bga/app-movil/ganamovil/frontend-react-native.git
cd frontend-react-native
```

>**🚧⚠ Se debe crear una rama por cada tarea y/o función a crear y luego coordinar con los involucrados para el respectivo merge a: ``develop`` ⚠🚧**

Instala los paquetes necesarios para el proyecto con el siguiente desarrollo

```sh
npm i
```

## **Comandos básicos**

Abra la terminal de su preferencia y ejecute los comandos de su preferencia.

#### Iniciar con Android en Ambiente de Desarrollo

```sh
npm run android
```
#### Iniciar con Android en Ambiente de Producción

```sh
npm run android-release
```
#### Iniciar con IOS en Ambiente de Producción

```sh
npm run ios
```
#### Iniciar con IOS en Ambiente de Producción

```sh
npm run ios-release
```
#### (optional) En caso de que Metro no se ejecute de forma automática

```sh
npm start
```
#### Generar documentación

```sh
npm run docs
```

### **Paquetes para el ambiente de Producción**

Listado de paquetes que se está utilizando en producción.

| Paquete                        | Versión |
| ------------------------------ | ------- |
|@react-native-async-storage/async-storage |^1.17.10|
|@react-native-community/netinfo |^9.3.1|
|@react-navigation/native |^6.0.11|
|@react-navigation/native-stack |^6.7.0|
|@reduxjs/toolkit |^1.8.5|
|@testing-library/react-native |^11.0.0|
|axios |^0.27.2|
|i |^0.3.7|
|npm |^8.19.2|
|react |18.0.0|
|react-native |0.69.2|
|react-native-biometrics |^2.2.2|
|react-native-collapsible |^1.6.0|
|react-native-device-info |^10.1.2|
|react-native-dotenv |^3.3.1|
|react-native-geolocation-service |^5.3.0|
|react-native-linear-gradient |^2.6.2|
|react-native-maps |^1.1.0|
|react-native-safe-area-context |^4.3.1|
|react-native-screens |^3.15.0|
|react-native-svg |^12.4.0|
|react-redux |^8.0.2|

### **Paquetes para el ambiente de Desarrollo**

Listado de paquetes que se está utilizando en desarrollo.

| Paquete                               | Versión |
| ------------------------------------- | ------- |
|@babel/core |^7.12.9|
|@babel/runtime |^7.12.5|
|@react-native-community/eslint-config |^2.0.0|
|babel-jest |^26.6.3|
|clean-jsdoc-theme |^4.1.8|
|eslint |^8.23.1|
|eslint-config-prettier |^8.5.0|
|eslint-config-standard |^17.0.0|
|eslint-plugin-import |^2.26.0|
|eslint-plugin-n |^15.2.5|
|eslint-plugin-promise |^6.0.1|
|eslint-plugin-react |^7.31.8|
|jest |^26.6.3|
|jsdoc |^3.6.11|
|metro-react-native-babel-preset |^0.70.3|
|prettier |2.7.1|
|react-native-svg-transformer |^1.0.0|
|react-test-renderer |18.0.0|

## **Exportar para Google Play**
### **Generar apk de Arquitectura 32/64** ❗

Para ello primero se debe tener el archivo .keystore de GanaMóvil y agregarlo en la ubicación del proyecto **`./android/app`**. Y comience a ejecutar la siguiente lista de comandos:

```sh
cd ./android
```
> Asegurese de estar dentro de la carpeta android o tener la configuracion de Gradlew en el path.
```sh
./gradlew assembleRelease
```

#### **Generar AAB (Recomendado)** ✅

```sh
cd ./android
```
> Asegurese de estar dentro de la carpeta android o tener la configuracion de Gradlew en el path.
```sh
./gradlew bundleRelease
```
