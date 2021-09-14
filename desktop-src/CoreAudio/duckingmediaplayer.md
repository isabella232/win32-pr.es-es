---
description: Esta aplicación de ejemplo muestra la atenuación de secuencias mediante la implementación de un reproductor multimedia que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, opta por no recibir eventos de afijo e implementa un control personalizado cuando se reciben eventos de afijo.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: AficiónMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165014"
---
# <a name="duckingmediaplayer"></a>AficiónMediaPlayer

Esta aplicación de ejemplo muestra la atenuación de secuencias mediante la implementación de un reproductor multimedia que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, opta por no recibir eventos de afijo e implementa un control personalizado cuando se reciben eventos de afijo. Este ejemplo debe usarse en la conjuación [con ElojoCapturaEjemplo](duckingcapturesample.md). Para obtener más información sobre la atenuación de secuencias o el afijo, vea [Default Ducking Experience](stream-attenuation.md).

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   DirectShow reproducir un archivo multimedia.
-   [WASAPI para](wasapi.md) la administración de flujos y el control de eventos de afijo.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Los SDK de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ agachandoMediaPlayer... \\ |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo de DuckingMediaPlayer, siga estos pasos:

1.  Abra el archivo DuckingMediaPlayer.sln en Visual Studio 2008.
2.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre Visual Studio shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingMediaPlayer.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación correctamente, se genera un archivo ejecutable, DuckingMediaPlayer.exe, . Para ejecutarlo, seleccione **Iniciar depuración** **o** Iniciar sin depurar en el menú **Depurar** o escriba en una ventana de `DuckingMediaPlayer` comandos.

Para ver una demostración de la afición, debe ejecutar LanchaMediaPlayer y DuckingCaptureSample simultáneamente. La clase DuckingCaptureSample abre un flujo de comunicación y señala al sistema para que genere un evento de afijo. El sistema notifica a La clase DuckingMediaPlayer cuando se produce un evento de afijo y el reproductor multimedia realiza la acción solicitada por el usuario.

Para deshabilitar el comportamiento de la afición:

1.  En la ventana DuckingCaptureSample, seleccione **Usar**  dispositivo de entrada predeterminado y haga clic en Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En el botón DesancharMediaPlayer, seleccione un archivo multimedia para reproducir y especifique la opción de afijo como **No participar en la reproducción.**

Observe que el archivo multimedia se reproduce sin interrupción. Se omiten los eventos generados por el sistema cuando se abre el flujo de comunicación.

Para demostrar el comportamiento predeterminado de la afición proporcionada por el sistema, haga lo siguiente:

1.  Seleccione la **opción Sonidos** en el panel de control. En la **pestaña** Comunicaciones, **seleccione Reducir el volumen de otros sonidos en un 80 %.**
2.  En la ventana DuckingCaptureSample, seleccione **Usar**  dispositivo de entrada predeterminado y haga clic en Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
3.  En el botón DesaprobaciónMediaPlayer, seleccione un archivo multimedia para reproducirlo, sin elegir ninguna de las opciones de afijo.
4.  En la ventana DeteniendoCaptureSample, haga clic **en Detener** para detener el flujo de comunicación.

Tenga en cuenta que, cuando ElgingCaptureSample abre el flujo de comunicación, el archivo multimedia reproducido por DuckingMediaPlayer se reproduce sin interrupción, pero el nivel de volumen se reduce. Cuando se detiene la sesión de comunicación, el volumen se restablece a la configuración original. Este comportamiento de atenuación de flujo es el comportamiento predeterminado de afijo implementado por el sistema.

Para ver un comportamiento de afijo personalizado implementado por el reproductor multimedia:

1.  En la ventana DuckingCaptureSample, seleccione **Usar**  dispositivo de entrada predeterminado y haga clic en Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En el botón DesaprobaciónMediaPlayer, seleccione un archivo multimedia para reproducir y especifique la opción de afijo como **Pausar en el patón**.
3.  En la ventana DeteniendoCaptureSample, haga clic **en Detener** para detener el flujo de comunicación.

Tenga en cuenta que, cuando ElgingCaptureSample abre el flujo de comunicación, el archivo multimedia reproducido por DuckingMediaPlayer está en pausa. La reproducción se reanuda cuando se detiene la sesión de comunicación. Este comportamiento de atenuación de secuencia es el comportamiento de afijo implementado por el reproductor multimedia.

También se muestra cómo integrar el control de volumen para cada aplicación con el mezclador de volúmenes.

Para obtener más información sobre la característica de atenuación de secuencias, vea [Default Ducking Experience](stream-attenuation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos del SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



