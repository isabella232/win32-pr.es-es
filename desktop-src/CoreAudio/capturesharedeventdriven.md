---
description: Esta aplicación de ejemplo usa core Audio API para capturar datos de audio de un dispositivo de entrada especificado por el usuario y los escribe en un archivo .wav con nombre único en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165126"
---
# <a name="capturesharedeventdriven"></a>CaptureSharedEventDriven

Esta aplicación de ejemplo usa core Audio API para capturar datos de audio de un dispositivo de entrada especificado por el usuario y los escribe en un archivo .wav con nombre único en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   [MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.
-   [WASAPI para](wasapi.md) las operaciones de administración de flujos, como iniciar y detener la secuencia, y el cambio de secuencia.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa Sdk de Microsoft Windows archivos de audio multimedia de ejemplo \\ \\ \\ v7.0 \\ \\ \\ \\ CaptureSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo CaptureSharedEventDriven, siga estos pasos:

1.  Abra el shell de CMD para Windows SDK y cambie al directorio de ejemplo CaptureSharedEventDriven.
2.  Ejecute el comando en el directorio CaptureSharedEventDriven para abrir el proyecto `start WASAPICaptureSharedEventDriven.sln` WASAPICaptureSharedEventDriven en Visual Studio ventana.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPICaptureSharedEventDriven.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera WASAPICaptureSharedEventDriven.exe archivo ejecutable. Para ejecutarlo, escriba `WASAPICaptureSharedEventDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la captura en el dispositivo multimedia predeterminado.

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                |
|-----------------|------------------------------------------------------------|
| -?              | Muestra ayuda.                                                |
| -H              | Muestra ayuda.                                                |
| -l              | Latencia de captura de audio en milisegundos.                     |
| -d              | Duración de la captura de audio en segundos.                         |
| -M              | Deshabilita el uso de MMCSS.                                 |
| -console        | Use el dispositivo de consola predeterminado.                            |
| -communications | Use el dispositivo de comunicación predeterminado.                      |
| -multimedia     | Use el dispositivo multimedia predeterminado.                         |
| -endpoint       | Use el identificador de punto de conexión especificado en el valor del modificador. |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de captura. La consola predeterminada, la comunicación y los dispositivos multimedia aparecen seguidos de los dispositivos y los identificadores de punto de conexión. Si no se especifica ninguna duración, la secuencia de audio del dispositivo especificado se captura durante 10 segundos. La aplicación escribe los datos capturados en un archivo .wav con nombre único.

CaptureSharedEventDriven muestra el almacenamiento en búfer controlado por eventos. El cliente de audio del que se ha creado una instancia para este ejemplo está configurado para ejecutarse en modo compartido y el procesamiento del cliente del búfer de audio se hace controlado por eventos estableciendo la marca **\_ \_ EVENTCALLBACK AUDCLNT STREAMFLAGS** en la llamada a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize). En el ejemplo se muestra cómo el cliente debe proporcionar un identificador de eventos al sistema mediante una llamada [**al método IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) Una vez que se inicia la sesión de captura y se inicia la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que el cliente lo procese. Los datos de audio también se pueden procesar en un bucle controlado por temporizador. Este modo se muestra en el [ejemplo CaptureSharedTimerDriven.](capturesharedtimerdriven.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



