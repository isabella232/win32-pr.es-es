---
description: Esta aplicación de ejemplo muestra la atenuación de secuencias mediante la implementación de un reproductor multimedia que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, opta por no recibir eventos de achacamiento e implementa un control personalizado cuando se reciben eventos de achacamiento.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab5a469ec2a7fb1551980d0a08a758e8e8e8f522831dc2148b2d8fb222ecdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828286"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

Esta aplicación de ejemplo muestra la atenuación de secuencias mediante la implementación de un reproductor multimedia que muestra el comportamiento de atenuación predeterminado proporcionado por el sistema, opta por no recibir eventos de achacamiento e implementa un control personalizado cuando se reciben eventos de achacamiento. Este ejemplo debe usarse en conjuación con [DuckingCaptureSample](duckingcapturesample.md). Para obtener más información sobre la atenuación de la secuencia o el agachamiento, vea [Default Ducking Experience](stream-attenuation.md).

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
-   [WASAPI para](wasapi.md) la administración de flujos y el control de eventos de agachamiento.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación    | Ruta de acceso o dirección URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo DuckingMediaPlayer, siga estos pasos:

1.  Abra el archivo DuckingMediaPlayer.sln en Visual Studio 2008.
2.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingMediaPlayer.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación correctamente, se genera un archivo ejecutable, DuckingMediaPlayer.exe, . Para ejecutarlo, seleccione **Iniciar depuración** **o** Iniciar sin depurar en el menú **Depurar** o escriba en una ventana de `DuckingMediaPlayer` comandos.

Para ver una demostración del agachamiento, debe ejecutar DuckingMediaPlayer y DuckingCaptureSample simultáneamente. DuckingCaptureSample abre un flujo de comunicación y señala al sistema para que genere un evento de patito. El sistema notifica a DuckingMediaPlayer cuando se produce un evento de agachamiento y el reproductor multimedia realiza la acción solicitada por el usuario.

Para deshabilitar el comportamiento de agachamiento:

1.  En la ventana DuckingCaptureSample, seleccione Usar dispositivo de **entrada** predeterminado y haga clic **en** Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En DuckingMediaPlayer, seleccione un archivo multimedia para reproducir y especifique la opción de afijo como **Opt out of Ducking (No participar en el agachamiento).**

Observe que el archivo multimedia se reproduce sin interrupción. Se omiten los eventos generados por el sistema cuando se abre el flujo de comunicación.

Para demostrar el comportamiento predeterminado de agachamiento proporcionado por el sistema, haga lo siguiente:

1.  Seleccione la **opción Sonidos** en el panel de control. En la **pestaña** Comunicaciones, **seleccione Reducir el volumen de otros sonidos en un 80 %.**
2.  En la ventana DuckingCaptureSample, seleccione Usar dispositivo de **entrada** predeterminado y haga clic **en** Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
3.  En DuckingMediaPlayer, seleccione un archivo multimedia para reproducirlo, sin elegir ninguna de las opciones de agachamiento.
4.  En la ventana DuckingCaptureSample, haga clic **en Detener** para detener el flujo de comunicación.

Observe que cuando DuckingCaptureSample abre la secuencia de comunicación, el archivo multimedia reproducido por DuckingMediaPlayer se reproduce sin interrupción, pero el nivel de volumen se reduce. Cuando se detiene la sesión de comunicación, el volumen se restablece a la configuración original. Este comportamiento de atenuación de flujo es el comportamiento predeterminado de agachamiento implementado por el sistema.

Para ver un comportamiento de agachamiento personalizado implementado por el reproductor multimedia:

1.  En la ventana DuckingCaptureSample, seleccione Usar dispositivo de **entrada** predeterminado y haga clic **en** Iniciar para iniciar una sesión de captura desde el dispositivo de comunicación.
2.  En DuckingMediaPlayer, seleccione un archivo multimedia para reproducir y especifique la opción de patito **como Pause on Duck (Pausar en el patito).**
3.  En la ventana DuckingCaptureSample, haga clic **en Detener** para detener el flujo de comunicación.

Tenga en cuenta que cuando DuckingCaptureSample abre la secuencia de comunicación, se pausa el archivo multimedia reproducido por DuckingMediaPlayer. La reproducción se reanuda cuando se detiene la sesión de comunicación. Este comportamiento de atenuación de flujo es el comportamiento de atenuación implementado por el reproductor multimedia.

DuckingMediaPlayer también muestra cómo integrar el control de volumen para cada aplicación con el mezclador de volúmenes.

Para obtener más información sobre la característica de atenuación de flujos, vea [Default Ducking Experience](stream-attenuation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



