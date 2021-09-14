---
description: En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation.Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated or Obsolete SamplesRelated topics
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Muestras de SDK de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5482fabe5e4bfdfe5d451fd8ccb9c0ba0504a5ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263372"
---
# <a name="media-foundation-sdk-samples"></a>Muestras de SDK de Media Foundation

En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation.

-   [Ejemplos de codificación](#encoding-samples)
-   [Ejemplos de reproducción](#playback-samples)
-   [Complementos](#plug-ins)
-   [Ejemplos de lector de origen](#source-reader-samples)
-   [Captura de vídeo](#video-capture)
-   [Ejemplos varios](#miscellaneous-samples)
-   [Ejemplos obsoletos o en desuso](#deprecated-or-obsolete-samples)
-   [Temas relacionados](#related-topics)

## <a name="encoding-samples"></a>Ejemplos de codificación



| Muestra                            | Descripción                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcodificación](transcode-sample.md) | Muestra cómo volver a codificar un archivo multimedia para Windows formato multimedia. |



 

## <a name="playback-samples"></a>Ejemplos de reproducción



| Muestra                                            | Descripción                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Reproduce archivos de audio y vídeo mediante la [sesión multimedia](media-session.md). En este ejemplo se muestra cómo crear topologías de reproducción, controlar la sesión multimedia y recibir eventos de sesión durante la reproducción. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Muestra algunas funciones de reproducción que no se incluyen en el [ejemplo BasicPlayback.](/previous-versions//bb970475(v=vs.85))                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Reproduce archivos de audio y vídeo protegidos. En este ejemplo se muestra cómo usar la sesión de ruta de acceso multimedia protegida (PMP) y cómo usar objetos habilitador de contenido.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Muestra                                       | Sub-Area                         | Descripción                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Descodificador](decoder-sample.md)                | Media Foundation transformación (MFT) | Descodificador de vídeo.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Varios                    | Presentador personalizado para [el representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).                 |
| [AudioDelay de MFT \_](mft-audiodelay-sample.md) | MFT                              | Transformación de efecto de audio. Muestra cómo escribir un MFT básico para el procesamiento de audio.                           |
| [Escala de grises de MFT \_](mft-grayscale-sample.md)   | MFT                              | Efecto de vídeo de escala de grises. Muestra cómo escribir un MFT básico para el procesamiento de vídeo.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Origen multimedia                     | Analiza secuencias de capa de sistemas MPEG-1. Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes. |
| [WavSink](wavsink-sample.md)                | Receptor multimedia                       | Receptor de archivo que escribe archivos .wav. Muestra cómo escribir un receptor multimedia personalizado.                        |
| [WavSource](wavsource-sample.md)            | Origen multimedia                     | Analiza archivos .wav. Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes.                   |



 

## <a name="source-reader-samples"></a>Ejemplos de lector de origen



| Muestra                                      | Descripción                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Audio Clip](audio-clip-sample.md)         | Usa el [Lector de origen](source-reader.md) para descodificar el audio de un archivo multimedia.      |
| [VideoThumbnail](videothumbnail-sample.md) | Usa el [Lector de origen](source-reader.md) para obtener fotogramas únicos de un archivo de vídeo. |



 

## <a name="video-capture"></a>Captura de vídeo



| Muestra                                        | Descripción                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Muestra cómo obtener una vista previa del vídeo desde un dispositivo de captura de vídeo mediante Direct3D para representar el vídeo. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Muestra cómo capturar vídeo desde una cámara de vídeo a un archivo.                                   |



 

## <a name="miscellaneous-samples"></a>Ejemplos varios



| Muestra                                         | Descripción                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Muestra cómo analizar datos de un archivo de formato de sistemas avanzados (ASF).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Muestra cómo usar alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD).                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Usa DirectX Video Acceleration (DXVA) 2.0 para crear una secuencia de vídeo YUV de 4:2:2. En este ejemplo se muestra cómo usar las características de procesamiento de vídeo de DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Ejemplos obsoletos o en desuso




| Muestra | Descripción | 
|--------|-------------|
| <a href="mfplayer2-sample.md">MFPlayer2</a> | Muestra algunas características avanzadas de reproducción de la API <a href="using-mfplay-for-audio-video-playback.md">MFPlay.</a> | 
| <a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a> | Aplica un efecto de escala de grises al vídeo. Muestra cómo insertar mfts en una topología de reproducción.<br /><blockquote>[!Note]<br />Este ejemplo ya no se incluye en el SDK.</blockquote><br /> | 
| <a href="playlist-sample.md">Lista de reproducción</a> | Reproduce una secuencia de archivos de audio mediante el origen del secuenciador.<br /><blockquote>[!Note]<br />Este ejemplo ya no se incluye en el SDK.</blockquote><br /> | 
| <a href="simplecapture-sample.md">SimpleCapture</a> | Muestra cómo obtener una vista previa del vídeo desde un dispositivo de captura de vídeo mediante la API MFPlay. | 
| <a href="simpleplay-sample.md">SimplePlay</a> | Muestra cómo reproducir un archivo multimedia mediante la API MFPlay. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
