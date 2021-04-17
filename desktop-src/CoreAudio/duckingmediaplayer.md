---
description: En esta aplicación de ejemplo se muestra la atenuación de la secuencia mediante la implementación de un reproductor de media que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, no participa en la carga de eventos e implementa el control personalizado cuando se reciben eventos de la carga.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105660005"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

En esta aplicación de ejemplo se muestra la atenuación de la secuencia mediante la implementación de un reproductor de media que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, no participa en la carga de eventos e implementa el control personalizado cuando se reciben eventos de la carga. Este ejemplo se debe usar en conjuction con [DuckingCaptureSample](duckingcapturesample.md). Para obtener más información sobre la forma de uso de metadatos o de la atenuación de flujos, consulte [experiencia predeterminada de los patos](stream-attenuation.md).

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   DirectShow para reproducir un archivo multimedia.
-   [WASAPI](wasapi.md) para la administración de transmisiones y control de eventos de pato.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo DuckingMediaPlayer, siga estos pasos:

1.  Abra DuckingMediaPlayer. sln en Visual Studio 2008.
2.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingMediaPlayer. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación correctamente, se genera un archivo ejecutable DuckingMediaPlayer.exe. Para ejecutarlo, seleccione **iniciar depuración** o **iniciar sin depurar** en el menú **depurar** o escriba `DuckingMediaPlayer` en una ventana de comandos.

Para ver una demostración de la pato, debe ejecutar DuckingMediaPlayer y DuckingCaptureSample simultáneamente. DuckingCaptureSample abre un flujo de comunicación e indica al sistema que genere un evento de pato. El sistema notifica a DuckingMediaPlayer cuando se produce un evento de pato y el reproductor de media realiza la acción solicitada por el usuario.

Para deshabilitar el comportamiento de los patos:

1.  En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo y especifique la opción de patos como no **participar**.

Tenga en cuenta que el archivo multimedia se reproduce sin ninguna interrupción. Los eventos generados por el sistema cuando se omite el flujo de comunicación abierto.

Para demostrar el comportamiento de la forma predeterminada de los patos proporcionados por el sistema, haga lo siguiente:

1.  Seleccione la opción **sonidos** en el panel de control. En la pestaña **comunicaciones** , seleccione **reducir el volumen de otros sonidos en un 80%**.
2.  En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.
3.  En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo sin elegir ninguna de las opciones de pato.
4.  En la ventana DuckingCaptureSample, haga clic en **detener** para detener la secuencia de comunicación.

Tenga en cuenta que cuando DuckingCaptureSample abre la secuencia de comunicación, el archivo multimedia que reproduce DuckingMediaPlayer se reproduce sin interrupción, pero se reduce el nivel de volumen. Cuando se detiene la sesión de comunicación, el volumen se restablece a la configuración original. Este comportamiento de la atenuación de secuencias es el comportamiento de la forma predeterminada de los patos implementado por el sistema.

Para ver un comportamiento personalizado de patos implementado por el reproductor de media:

1.  En la ventana DuckingCaptureSample, seleccione **usar el dispositivo de entrada predeterminado** y haga clic en **iniciar** para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En el DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo y especifique la opción de la pato como **pausar en Duck**.
3.  En la ventana DuckingCaptureSample, haga clic en **detener** para detener la secuencia de comunicación.

Tenga en cuenta que cuando DuckingCaptureSample abre el flujo de comunicación, el archivo multimedia que reproduce DuckingMediaPlayer está en pausa. La reproducción se reanuda cuando se detiene la sesión de comunicación. Este comportamiento de la atenuación de secuencias es el comportamiento de los patos implementado por el reproductor de media.

DuckingMediaPlayer también muestra cómo integrar el control de volumen para cada aplicación con el mezclador de volumen.

Para obtener más información acerca de la característica de atenuación de flujos, consulte [experiencia predeterminada](stream-attenuation.md)de la misma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



