---
description: En este ejemplo se usan las API core audio para capturar una secuencia de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante el uso del AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft .
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7960a1ff3163b936af949d605e7782f8a09890741f99e022c37a0aadc57a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059125"
---
# <a name="aecmicarray"></a>AECMicArray

En este ejemplo se usan las API core audio para capturar una secuencia de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante el uso del AEC DMO, también denominado DSP de captura de voz, proporcionado por Microsoft .

Este tema contiene las secciones siguientes.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   [MMDevice para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.
-   [WASAPI para](wasapi.md) operaciones de administración de flujos, como iniciar y detener la secuencia, el cambio de secuencia.
-   [DeviceTopology para](devicetopology-api.md) enumerar adaptadores de audio.
-   [EndpointVolume](endpointvolume-api.md) controla los niveles de volumen de [las sesiones de audio.](audio-sessions.md)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión                     |
|----------------------------------------------------------------|-----------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o posterior      |
| Visual Studio                                                  | 2005 (ediciones no express) |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación    | Ruta de acceso o dirección URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa Sdk de Microsoft Windows audio multimedia de ejemplo \\ \\ \\ v7.0 \\ \\ \\ \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo AecSDKDemo, siga estos pasos:

1.  Abra una ventana de comandos del SDK.
2.  Escriba **cd %MSSDK% \\ Setup**.
3.  Ejecute VCIntegrate.exe.

    A partir de este momento, las ventanas de comandos tendrán la configuración de entorno adecuada para compilar una aplicación que aproveche las ventajas del SDK.

4.  Compile el ejemplo.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera un archivo ejecutable AecSDKDemo.exe aplicación. Para ejecutarlo, escriba `AecSDKDemo` una ventana de comandos seguida de argumentos obligatorios u opcionales, como se describe a continuación.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

En la tabla siguiente se muestran los argumentos.

| Argumento  | Descripción                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obligatorio. Especifica el nombre del archivo de salida.                                                                                                 |
| -mod      | Obligatorio. Especifica el modo del sistema de captura de voz. Consulte la sección "Configuración de la captura de DMO" del archivo Léame de ejemplo para obtener más información. |
| -feat     | Opcional. Activa o desactiva el modo de característica (1) o desactivado (0).                                                                                       |
| -ns       | Opcional. Activa o desactiva la supresión de ruido (1) o desactivada (0). El modo de característica debe estar en para especificarlo.                                     |
| -agc      | Opcional. Activa o desactiva AGC digital (1) o desactivada (0). El modo de característica debe estar en para especificarlo.                                           |
| -cntrclip | Opcional. Activa o desactiva el recorte del centro (1) o desactivado (0). El modo de característica debe estar en para especificarlo.                                       |
| -spkdev   | Opcional. Especifica el índice del dispositivo del hablante. Si no se especifica, se le pedirá al usuario que seleccione.                                         |
| -micdev   | Opcional. Especifica el índice del dispositivo de micrófono. Si no se especifica, se le pedirá al usuario que seleccione.                                      |
| -duration | Opcional. Especifica cuánto tiempo se ejecuta la aplicación.                                                                                    |



 

Esta aplicación de ejemplo no reproduce ninguna señal. Para ejecutar la demostración correctamente para los modos habilitados para AEC (modo 0 y 4), los usuarios deben reproducir algunas señales de audio a través del mismo dispositivo de altavoz especificado para el DMO (es decir, el dispositivo especificado por la opción "-spkdev"), que simula la voz de extremo a extremo en un escenario de chat de dos vías. Los usuarios pueden usar cualquier reproductor para reproducir cualquier señal de audio. Si no hay ninguna secuencia de representación activa en el dispositivo de altavoz seleccionado, el DMO no se podrá procesar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



