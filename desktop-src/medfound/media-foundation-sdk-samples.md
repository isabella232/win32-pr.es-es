---
description: En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated u obsoleto SamplesRelated temas
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Muestras de SDK de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820247"
---
# <a name="media-foundation-sdk-samples"></a>Muestras de SDK de Media Foundation

En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation.

-   [Ejemplos de codificación](#encoding-samples)
-   [Ejemplos de reproducción](#playback-samples)
-   [Complementos de](#plug-ins)
-   [Ejemplos de lector de código fuente](#source-reader-samples)
-   [Captura de vídeo](#video-capture)
-   [Varios ejemplos](#miscellaneous-samples)
-   [Ejemplos desusados u obsoletos](#deprecated-or-obsolete-samples)
-   [Temas relacionados](#related-topics)

## <a name="encoding-samples"></a>Ejemplos de codificación



| Muestra                            | Descripción                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcodificar](transcode-sample.md) | Muestra cómo recodificar un archivo multimedia en el formato de Windows Media. |



 

## <a name="playback-samples"></a>Ejemplos de reproducción



| Muestra                                            | Descripción                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Reproduce archivos de audio y vídeo mediante la [sesión multimedia](media-session.md). Este ejemplo muestra cómo crear topologías de reproducción, controlar la sesión multimedia y recibir eventos de sesión durante la reproducción. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Muestra algunas funciones de reproducción que no se incluyen en el ejemplo [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Reproduce archivos de audio y vídeo protegidos. En este ejemplo se muestra cómo usar la sesión de la ruta de acceso a medios protegidos (PMP) y cómo usar objetos de habilitador de contenido.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Muestra                                       | Sub-Area                         | Descripción                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Descodificador](decoder-sample.md)                | Media Foundation Transform (MFT) | Descodificador de vídeo.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Varios                    | Presentador personalizado para el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).                 |
| [AudioDelay de MFT \_](mft-audiodelay-sample.md) | MAESTRA                              | Transformación de efecto de audio. Muestra cómo escribir una MFT básica para el procesamiento de audio.                           |
| [\_Escala de grises de MFT](mft-grayscale-sample.md)   | MAESTRA                              | Efecto de vídeo de escala de grises. Muestra cómo escribir una MFT básica para el procesamiento de vídeo.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Origen de medios                     | Analiza los flujos de capas de sistemas MPEG-1. Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes. |
| [WavSink](wavsink-sample.md)                | Receptor de medios                       | Un receptor de archivo que escribe archivos. wav. Muestra cómo escribir un receptor de multimedia personalizado.                        |
| [WavSource](wavsource-sample.md)            | Origen de medios                     | Analiza los archivos. wav. Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes.                   |



 

## <a name="source-reader-samples"></a>Ejemplos de lector de código fuente



| Muestra                                      | Descripción                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Clip de audio](audio-clip-sample.md)         | Utiliza el [lector de origen](source-reader.md) para descodificar el audio de un archivo multimedia.      |
| [Videominiatura](videothumbnail-sample.md) | Utiliza el [lector de origen](source-reader.md) para obtener fotogramas individuales de un archivo de vídeo. |



 

## <a name="video-capture"></a>Captura de vídeo



| Muestra                                        | Descripción                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo, usando Direct3D para representar el vídeo. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Muestra cómo capturar vídeo de una cámara de vídeo a un archivo.                                   |



 

## <a name="miscellaneous-samples"></a>Varios ejemplos



| Muestra                                         | Descripción                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Muestra cómo analizar los datos de un archivo de formato de sistema avanzado (ASF).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).                                                                      |
| [Videoproc DXVA2 \_](dxva2-videoproc-sample.md) | Usa la aceleración de vídeo de DirectX (DXVA) 2,0 para crear un flujo de vídeo 4:2:2 YUV. En este ejemplo se muestra cómo usar las características de procesamiento de vídeo de DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Ejemplos desusados u obsoletos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Muestra</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>Muestra algunas características de reproducción avanzada de la API de <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></td>
<td>Aplica un efecto de escala de grises a un vídeo. Muestra cómo insertar MFTs en una topología de reproducción.<br/>
<blockquote>
[!Note]<br />
Este ejemplo ya no se incluye en el SDK de.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">Lista de reproducción</a></td>
<td>Reproduce una secuencia de archivos de audio mediante el origen del secuenciador.<br/>
<blockquote>
[!Note]<br />
Este ejemplo ya no se incluye en el SDK de.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">SimpleCapture</a></td>
<td>Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo mediante la API de MFPlay.</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">SimplePlay</a></td>
<td>Muestra cómo reproducir un archivo multimedia mediante la API de MFPlay.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
