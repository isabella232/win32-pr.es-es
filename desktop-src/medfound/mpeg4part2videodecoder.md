---
description: El descodificador de vídeo MPEG4 parte 2 descodifica secuencias de vídeo codificadas según el estándar MPEG4 parte 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Descodificador de vídeo MPEG-4 parte 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275837"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Descodificador de vídeo MPEG-4 parte 2

El descodificador de vídeo MPEG4 parte 2 descodifica secuencias de vídeo codificadas según el estándar MPEG4 parte 2.

Puede crear una instancia del descodificador de vídeo MPEG4 Part 2 llamando a **CoCreateInstance**. Para crear una instancia del descodificador que se comporta como un objeto multimedia de DirectX (DMO), use el identificador de clase **CLSID \_ CMpeg4sDecMediaObject**. Para crear un Istance del descodificador que se comporta como una transformación de Media Foundation (MFT), use el identificador de clase **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Tipos de entrada

El descodificador de vídeo MPEG4 parte 2 admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ MP4 (desusado)
-   MEDIASUBTYPE \_ MP4 (desusado)

## <a name="output-types"></a>Tipos de salida

El descodificador de vídeo MPEG4 parte 2 admite los siguientes subtipos de medios de salida cuando actúa como DMO.

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

El descodificador de vídeo MPEG4 parte 2 admite los siguientes subtipos de medios de salida cuando actúa como MFT.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formatos

El descodificador de vídeo MPEG4 parte 2 acepta los siguientes formatos.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (solo se usa la parte VIH2 del encabezado).

## <a name="interfaces-for-the-dmo"></a>Interfaces para DMO

Si crea una instancia del descodificador de vídeo MPEG4 Part 2 como DMO, el descodificador expone las siguientes interfaces.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Puede obtener una interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) llamando a **CoCreateInstance** y puede obtener una interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) llamando a **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Interfaces para MFT

Si crea una instancia del descodificador de vídeo MPEG2 parte 2 como MFT, el descodificador expone las siguientes interfaces.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Puede obtener un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) llamando a **CoCreateInstance** y puede obtener un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) llamando a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Puede obtener un puntero a la interfaz [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) llamando a **QueryInterface** en MFT. Puede obtener un puntero a la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y pasando el servicio de control de **\_ tasa MF \_ \_** del identificador de servicio.

## <a name="profiles-and-levels"></a>Perfiles y niveles

La especificación MPEG4 define varios perfiles, cada uno de los cuales especifica las herramientas que un codificador puede utilizar para generar una secuencia codificada. El descodificador de vídeo MPEG4 "part2 admite dos de estos perfiles: perfil visual simple y perfil simple avanzado. En otras palabras, el descodificador de vídeo MPEG4 parte 2 puede descodificar flujos codificados según el perfil visual simple o el perfil simple avanzado.

El perfil visual simple admite la transmisión básica de vídeo de velocidad de bits baja en modo progresivo. Solo admite imágenes intra y de predicción. También admite el modo de encabezado corto, que es compatible con versiones anteriores del perfil de línea base H. 263. A partir de Windows 10, el descodificador de vídeo MPEG-4 parte 2 también admite H. 263v2 (H. 263 +), que admite tamaños de imagen personalizados.

El perfil simple avanzado es compatible con todas las herramientas del perfil visual simple y, además, admite vídeo entrelazado, fotogramas B, compensación de movimiento de PEL, tablas de cuantificación adicionales y compensación de movimiento global.

La especificación MPEG4 también define varios niveles, cada uno de los cuales especifica restricciones en el flujo de salida generado por un codificador.

En la tabla siguiente se muestran los perfiles y niveles, junto con las resoluciones típicas, que admite el descodificador de vídeo MPEG4 Part 2.



| Perfil         | Nivel | Resolución típica |
|-----------------|-------|--------------------|
| Objetos visuales simples   | 0     | 176 x 144          |
| Objetos visuales simples   | 1     | 176 x 144          |
| Objetos visuales simples   | 2     | 352 x 288          |
| Objetos visuales simples   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Objetos visuales simples   | 5     | 720 x 576          |
| Avanzado simple | 0     | 176 x 144          |
| Avanzado simple | 1     | 176 x 144          |
| Avanzado simple | 2     | 352 x 288          |
| Avanzado simple | 3     | 352 x 288          |
| Avanzado simple | 3b    | 352 x 288          |
| Avanzado simple | 4     | 352 x 756          |
| Avanzado simple | 5     | 720 x 576          |



 

Para obtener más información acerca de los perfiles y los niveles, consulte la especificación MPEG4 parte 2 (ISO/IEC 14496-2): tecnología de la información: codificación de objetos de audio visual, parte 2: visual.

## <a name="decoder-properties"></a>Propiedades del descodificador

Para establecer las propiedades en el descodificador de vídeo MPEG4 parte 2, use la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

El descodificador de vídeo MPEG4 parte 2 admite las siguientes propiedades.



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



 

## <a name="remarks"></a>Observaciones

Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT. Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT. Para obtener información sobre los GUID que representan subtipos de medios, consulte [tipos de medios](media-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
