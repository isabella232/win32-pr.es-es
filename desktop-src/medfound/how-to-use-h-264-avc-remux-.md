---
description: En este tema se describe cuándo y cómo usar un receptor H.264/AVC Remux MFT y MP4.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Cuándo y cómo usar H.264/AVC Remux MFT y mp4 sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357955"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Cuándo y cómo usar H.264/AVC Remux MFT y mp4 sink

En este tema se describe cuándo y cómo usar un receptor H.264/AVC Remux MFT y MP4.

## <a name="when-to-use-h264avc-remux-mft"></a>Cuándo usar H.264/AVC Remux MFT

El formato de archivo MPEG-4 requiere que cada muestra comprimida contenga una imagen principal con unidades NAL en el orden correcto. (Consulte la definición de la imagen principal y el orden obligatorio de las unidades NAL en la sección 7.4.1.2.3, Orden de **unidades NAL** e imágenes codificadas y asociación a las unidades de acceso , de la especificación H.264 AVC). También requiere que cada muestra comprimida esté asociada a una marca de tiempo de presentación, a la marca de tiempo de decodificación y a la duración de la muestra.

En muchos escenarios en los que las aplicaciones necesitan grabar vídeo H.264/AVC en un contenedor de archivos MPEG-4, es posible que el ejemplo comprimido no cumpla los requisitos anteriores. Por ejemplo, una muestra comprimida podría no contener una imagen principal completa o no tener asociada una marca de tiempo de presentación correcta. Algunos ejemplos de aplicación son:

-   Escriba vídeo elemental de streaming H.264/AVC en el contenedor de archivos MPEG-4.
-   Grabe el vídeo elemental H.264/AVC capturado por la cámara en el contenedor de archivos MPEG-4.
-   Grabar la videoconferencia H.264/AVC en el contenedor de archivos MPEG-4.
-   Concatene dos vídeos H.264/AVC en MPEG-2 TS o MP4 y escriba en el contenedor de archivos MPEG-4 con las marcas de tiempo correctas.
-   Vídeo remux H.264/AVC de AVCHD, formato de archivo MPEG-2 TS/PS al formato de archivo MPEG-4.
-   Recorte el archivo de vídeo H.264/AVC sin transcodificación.

En esta situación, la aplicación debe usar un MFT de remux H.264/AVC para convertir las muestras comprimidas que no contienen una imagen principal completa antes de que se escriban en el contenedor de archivos MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Uso del receptor H.264/AVC Remux MFT y MP4

Establezca el tipo de medio de salida de origen **en MFVideoFormat \_ H264 \_ ES**, lo que indica que es posible que cada muestra no contenga una imagen principal completa. Establezca el tipo de medio de entrada del receptor MP4 **en MFVideoFormat \_ H264.** Por lo tanto, el tipo de medio de entrada del MFT de remux H.264/AVC es **MFVideoFormat \_ H264 \_ ES** y el tipo de medio de salida del MFT de remux H.264/AVC es **MFVideoFormat \_ H264,** que se insertará automáticamente en la resolución de topología.

El remux H.264/AVC omite la duración de la muestra, ya que la duración de la muestra para una muestra que no contiene una imagen principal completa no tiene un significado claro. En su lugar, la duración de la muestra se calcula a partir de la velocidad de fotogramas. La velocidad de fotogramas se calcula a partir del parámetro de secuencia. Si la información no existe en el parámetro de secuencia, la velocidad de fotogramas se calcula a partir de los parámetros del tipo de medio de entrada. Si la información de velocidad de fotogramas no está disponible, se usa la velocidad de fotogramas predeterminada de 29,97 fps.

H.264/AVC remux MFT interpola linealmente las marcas de tiempo de decodificación (DTS) para cada imagen comprimida según la velocidad de fotogramas. H.264/AVC remux MFT respeta las marcas de tiempo de presentación de entrada (PTS) en los ejemplos de entrada y las pasa a la salida si existen. Realiza la interpolación de PTS según la velocidad de fotogramas, el PTS anterior y el orden de salida de la imagen a través del proceso de protuberancias de almacenamiento en búfer de imágenes descodificadas (DBP), tal y como se especifica en el anexo **C.4.5.3 Proceso** de protuberancia de la especificación H.264 AVC. Cada muestra de salida de H.264/AVC remux MFT debe tener PTS, DTS y duración de la muestra. H.264/AVC remux MFT también identifica las imágenes de IDR en el flujo de bits y las establece como punto limpio con el atributo MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Actualmente, el MFT de remux H.264/AVC puede controlar un máximo de 64 fotogramas reordenados. Si el número de fotogramas reordenados supera los 64 con un marco de referencia a largo plazo presente, el MFT de remux H.264/AVC interpolará un PTS incorrecto para ese fotograma y mostrará ese fotograma en un momento incorrecto.

Para crear una instancia de un MFT de remux H.264/AVC, establezca los tipos de medios de entrada y salida correctos en el MFT de remux H.264/AVC, establezca el tipo de medio de entrada para el receptor MP4 y resuelva la topología.

El código de ejemplo siguiente muestra cómo inicializar el receptor MFT y MP4 de remux H.264/AVC.

Para H.264/AVC remux MFT,


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



No es necesario realizar ninguna otra configuración.

Para el receptor MP4,


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



