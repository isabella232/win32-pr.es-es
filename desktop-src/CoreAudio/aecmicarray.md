---
description: En este ejemplo se usan las API de audio principales para capturar una secuencia de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153526"
---
# <a name="aecmicarray"></a>AECMicArray

En este ejemplo se usan las API de audio principales para capturar una secuencia de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft.

Este tema contiene las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   [MMDevice](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.
-   [WASAPI](wasapi.md) para las operaciones de administración de secuencias como el inicio y la detención de la secuencia, la conmutación por secuencias.
-   [DeviceTopology](devicetopology-api.md) para enumerar los adaptadores de audio.
-   [EndpointVolume](endpointvolume-api.md) controlan los niveles de volumen de las [sesiones de audio](audio-sessions.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión                     |
|----------------------------------------------------------------|-----------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o posterior      |
| Visual Studio                                                  | 2005 (ediciones que no son Express) |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo AecSDKDemo, siga estos pasos:

1.  Abra una ventana de comandos del SDK.
2.  Escriba **CD% MSSDK% \\ setup**.
3.  Ejecute VCIntegrate.exe.

    A partir de este momento, las ventanas de comandos tendrán la configuración de entorno adecuada para compilar una aplicación que aprovecha el SDK.

4.  Compile el ejemplo.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable AecSDKDemo.exe. Para ejecutarlo, escriba `AecSDKDemo` en una ventana de comandos seguida de los argumentos obligatorios u opcionales, tal y como se describe a continuación.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

En la tabla siguiente se muestran los argumentos.

| Argumento  | Descripción                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obligatorio. Especifica el nombre del archivo de salida.                                                                                                 |
| -mod      | Obligatorio. Especifica el modo del sistema de captura de voz. Consulte la sección "configuración de la captura de voz DMO" del archivo Léame de ejemplo para obtener más información. |
| -feat     | Opcional. Activa el modo de característica en (1) o desactivado (0).                                                                                       |
| -NS       | Opcional. Activa la supresión de ruido en (1) o desactivado (0). El modo de característica debe estar activado para especificar esto.                                     |
| -AGC      | Opcional. Desactiva el AGC digital (1) o desactivado (0). El modo de característica debe estar activado para especificar esto.                                           |
| -cntrclip | Opcional. Activa el recorte central en (1) o desactivado (0). El modo de característica debe estar activado para especificar esto.                                       |
| -spkdev   | Opcional. Especifica el índice de dispositivo de altavoz. Si no se especifica, se le pedirá al usuario que seleccione.                                         |
| -micdev   | Opcional. Especifica el índice del dispositivo de micrófono. Si no se especifica, se le pedirá al usuario que seleccione.                                      |
| -duración | Opcional. Especifica cuánto tiempo se ejecuta la aplicación.                                                                                    |



 

Esta aplicación de ejemplo no reproduce señales. Para ejecutar la demostración correctamente para los modos habilitados para AEC (modo 0 y 4), los usuarios deben reproducir algunas señales de audio a través del mismo dispositivo de altavoz especificado para DMO (es decir, el dispositivo especificado por la opción "-spkdev"), que simula la voz de un extremo en un escenario de charla bidireccional. Los usuarios pueden usar cualquier reproductor para reproducir señales de audio. Si no hay ningún flujo de representación activo en el dispositivo de altavoz seleccionado, el DMO no se procesará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



