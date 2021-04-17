---
description: En este tema se describe cuándo y cómo usar una MFT y un receptor MP4 de H. 264/AVC Remux.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Cuándo y cómo usar H. 264/AVC Remux MFT y el receptor MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706214"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Cuándo y cómo usar H. 264/AVC Remux MFT y el receptor MP4

En este tema se describe cuándo y cómo usar una MFT y un receptor MP4 de H. 264/AVC Remux.

## <a name="when-to-use-h264avc-remux-mft"></a>Cuándo usar H. 264/AVC Remux MFT

El formato de archivo MPEG-4 requiere que cada ejemplo comprimido contenga una imagen principal con unidades NAL en el orden correcto. (Consulte la definición de la imagen principal y el orden obligatorio de las unidades de NAL en la sección 7.4.1.2.3, el **orden de las unidades nal e imágenes codificadas y la asociación con las unidades de acceso** de la especificación H. 264 AVC). También requiere que cada ejemplo comprimido esté asociado a una marca de tiempo de presentación, la marca de tiempo de descodificación y la duración de la muestra.

En muchos escenarios en los que las aplicaciones necesitan grabar vídeo H. 264/AVC en un contenedor de archivos MPEG-4, el ejemplo comprimido podría no cumplir los requisitos anteriores. Por ejemplo, un ejemplo comprimido podría no contener una imagen principal completa o podría no tener asociada una marca de tiempo de presentación correcta. Algunos ejemplos de aplicaciones son:

-   Escriba el vídeo elemental de streaming H. 264/AVC en el contenedor de archivos MPEG-4.
-   Grabe vídeo capturado H. 264/AVC elemental en el contenedor de archivos MPEG-4.
-   Grabe la videoconferencia H. 264/AVC en el contenedor de archivos MPEG-4.
-   Concatene dos vídeo H. 264/AVC en MPEG-2 TS o MP4 y escriba en el contenedor de archivos MPEG-4 con las marcas de tiempo correctas.
-   Remux H. 264/AVC vídeo desde AVCHD, formato de archivo MPEG-2 TS/PS a formato de archivo MPEG-4.
-   Recorte el archivo de vídeo H. 264/AVC sin transcodificar.

En esta situación, la aplicación debe usar una MFT de H. 264/AVC Remux para convertir los ejemplos comprimidos que no contienen una imagen principal completa antes de que se escriban en el contenedor de archivos MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Uso de la MFT y el receptor MP4 de H. 264/AVC Remux

Establezca el tipo de medio de salida de origen en **MFVideoFormat \_ H264 \_ es**, lo que indica que cada ejemplo podría no contener una imagen principal completa. Establezca el tipo de medio de entrada del receptor de MP4 en **MFVideoFormat \_ H264**. Por lo tanto, el tipo de medio de entrada del MFT H. 264/AVC Remux es **MFVideoFormat \_ H264 \_** es y el tipo de medio de salida de la MFT h. 264/AVC Remux es **MFVideoFormat \_ H264**, que se insertará automáticamente en la resolución de la topología.

La duración de ejemplo se omite en H. 264/AVC Remux, porque la duración de la muestra para una muestra que no contiene una imagen principal completa no tiene un significado claro. En su lugar, la duración de la muestra se calcula a partir de la velocidad de fotogramas. La velocidad de fotogramas se calcula a partir del parámetro de secuencia. Si la información no existe en el parámetro Sequence, la velocidad de fotogramas se calcula a partir de los parámetros del tipo de medio de entrada. Si la información de velocidad de fotogramas no está disponible, se usa la velocidad de fotogramas predeterminada de 29,97 fps.

H. 264/AVC Remux MFT interpola linealmente las marcas de tiempo de descodificación (DTS) de cada imagen comprimida según la velocidad de fotogramas. H. 264/AVC Remux MFT respeta las marcas de tiempo de presentación de entrada (PTS) en los ejemplos de entrada y los pasa a la salida si existen. Realiza la interpolación PTS de acuerdo con la velocidad de fotogramas, el PTS anterior y el orden de salida de la imagen a través del proceso de rugosidad del almacenamiento en búfer de imágenes (DBP), tal y como se especifica en el **Anexo C. 4.5.3** de la especificación H. 264 AVC. Cada ejemplo de salida de la MFT H. 264/AVC Remux debe tener PTS, DTS y la duración de la muestra. La MFT H. 264/AVC Remux también identifica las imágenes de IDR en el fragmentada y las establece como punto de limpieza con el atributo MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Actualmente, la MFT de H. 264/AVC Remux puede controlar un máximo de 64 fotograma reordenado. Si el número de fotogramas reordenados supera el valor de 64 con un marco de referencia a largo plazo, el MFT de H. 264/AVC Remux interpolará un valor de PTS equivocado para ese fotograma y generará ese fotograma en un momento equivocado.

Para crear una instancia de un MFT de H. 264/AVC Remux, establezca los tipos de medios de entrada y salida correctos en la MFT H. 264/AVC Remux, establezca el tipo de medio de entrada para el receptor MP4 y resuelva la topología.

En el código de ejemplo siguiente se muestra cómo inicializar la MFT de H. 264/AVC Remux y el receptor MP4.

Para MFT Remux de H. 264/AVC,


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

 

 



