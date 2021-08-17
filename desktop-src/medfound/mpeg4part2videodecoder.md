---
description: El descodificador MPEG4 Part 2 Video descodifica secuencias de vídeo codificadas según el estándar MPEG4 Parte 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Descodificador de vídeo MPEG-4, parte 2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847e5be8c506e534c42962ecf6b0037a2ecb2f184c9c47fa92981fa32fd55422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973024"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Descodificador de vídeo MPEG-4, parte 2

El descodificador MPEG4 Part 2 Video descodifica secuencias de vídeo codificadas según el estándar MPEG4 Parte 2.

Puede crear una instancia del descodificador mpeg4, parte 2, vídeo llamando **a CoCreateInstance**. Para crear una instancia del descodificador que se comporte como un objeto multimedia DirectX (DMO), use el identificador de clase **CLSID \_ CMpeg4sDecMediaObject**. Para crear una posición del descodificador que se comporte como una transformación de Media Foundation (MFT), use el identificador de clase **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Tipos de entrada

El descodificador MPEG4 Part 2 Video admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ MP4S (en desuso)
-   MEDIASUBTYPE \_ mp4s (en desuso)

## <a name="output-types"></a>Tipos de salida

El descodificador de vídeo MPEG4, parte 2, admite los siguientes subtipos de medios de salida cuando actúa como un DMO.

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

El descodificador de vídeo MPEG4, parte 2, admite los siguientes subtipos de medios de salida cuando actúa como MFT.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formatos

El descodificador de vídeo MPEG4, parte 2, acepta los siguientes formatos.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (solo se usa la parte del encabezado MPEG2).

## <a name="interfaces-for-the-dmo"></a>Interfaces para el DMO

Si crea una instancia del descodificador MPEG4 Part 2 Video como DMO, el descodificador expone las interfaces siguientes.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Puede obtener una [**interfaz IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) llamando a **CoCreateInstance** y puede obtener una interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) llamando a **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Interfaces para MFT

Si crea una instancia del descodificador MPEG2 Part 2 Video como MFT, el descodificador expone las interfaces siguientes.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Puede obtener un puntero a la interfaz [**DETRANSFORMTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) mediante una llamada a **CoCreateInstance** y puede obtener un puntero a la interfaz [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) mediante una llamada a [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Puede obtener un puntero a la interfaz [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**ASEQUALITYAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) llamando a **QueryInterface** en el MFT. Puede obtener un puntero a la interfaz [**MFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**ASERATESupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y pasando el identificador de servicio **MF RATE CONTROL \_ \_ \_ SERVICE**.

## <a name="profiles-and-levels"></a>Perfiles y niveles

La especificación MPEG4 define varios perfiles, cada uno de los cuales especifica las herramientas que un codificador puede usar para generar una secuencia codificada. El descodificador de vídeo MPEG4 Part2 admite dos de esos perfiles: Perfil visual simple y Perfil simple avanzado. En otras palabras, el descodificador MPEG4 Part 2 Video puede descodificar secuencias codificadas según el perfil visual simple o el perfil simple avanzado.

El perfil visual simple admite la transmisión básica de vídeo de velocidad de bits baja en modo progresiva. Solo admite imágenes dentro de y predicción. También admite el modo de encabezado corto, que es compatible con versiones anteriores con el perfil de línea base H.263. A partir Windows 10, el descodificador de vídeo MPEG-4, parte 2, también admite H.263v2 (H.263+), que admite tamaños de imagen personalizados.

El perfil simple avanzado admite todas las herramientas del perfil visual simple y, además, admite vídeo entrelazado, fotogramas B, compensación de movimiento de trimestre, tablas de cuantificación adicionales y compensación de movimiento global.

La especificación MPEG4 también define varios niveles, cada uno de los cuales especifica restricciones en el flujo de salida generado por un codificador.

En la tabla siguiente se muestran los perfiles y niveles, junto con las resoluciones típicas, compatibles con el descodificador mpeg4, parte 2, vídeo.



| Perfil         | Nivel | Resolución típica |
|-----------------|-------|--------------------|
| Simple Visual   | 0     | 176 x 144          |
| Simple Visual   | 1     | 176 x 144          |
| Simple Visual   | 2     | 352 x 288          |
| Simple Visual   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Simple Visual   | 5     | 720 x 576          |
| Advanced Simple | 0     | 176 x 144          |
| Advanced Simple | 1     | 176 x 144          |
| Advanced Simple | 2     | 352 x 288          |
| Advanced Simple | 3     | 352 x 288          |
| Advanced Simple | 3b    | 352 x 288          |
| Advanced Simple | 4     | 352 x 756          |
| Advanced Simple | 5     | 720 x 576          |



 

Para obtener más información sobre los perfiles y los niveles, vea la especificación MPEG4 Parte 2 (ISO/IEC 14496-2): Tecnología de la información-- Codificación de objetos audio visuales -- Parte 2: Visual.

## <a name="decoder-properties"></a>Propiedades del descodificador

Para establecer propiedades en el descodificador mpeg4, parte 2, vídeo, use la [**interfaz ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o [**la interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

El descodificador MPEG4 Part 2 Video admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
<th>Valor predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Especifica el nivel de energía.<br/> <dl> Windows 7.<br />
De solo escritura.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Especifica el modo de generación de miniaturas.<br/> <dl> Windows 7.<br />
De solo escritura.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Los identificadores únicos globales (GUID) de los subtipos de medios RGB difieren en función de si un descodificador actúa como DMO o MFT. Los GUID de los subtipos multimedia no RGB son los mismos, independientemente de si un descodificador actúa como DMO o MFT. Para obtener información sobre los GUID que representan subtipos de medios, vea [Tipos de medios](media-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
