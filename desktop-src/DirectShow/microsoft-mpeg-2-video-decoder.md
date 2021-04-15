---
description: Este filtro descodifica el vídeo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Descodificador de vídeo MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422802"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Descodificador de vídeo MPEG-2 de Microsoft

Este filtro descodifica el vídeo MPEG-1, MPEG-2, H. 264.

> [!Note]  
> La descodificación del vídeo H. 264 requiere Windows 7.

 

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 

En el registro, el nombre descriptivo de este filtro es "Microsoft DTV-DVD video descodificador".



Información de filtro

Interfaces de filtro

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de medios de anclaje de entrada

PIN de entrada de vídeo:

-   \_ \_ Paquete cifrado \_ de DVD de MEDIATYPE, vídeo de MEDIASUBTYPE \_ MPEG2 \_
-   \_Vídeo MPEG2 \_ de MEDIATYPE, MEDIASUBTYPE \_ MPEG2 \_
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MPEG1Payload
-   Vídeo \_ de MEDIATYPE, \_ vídeo de MEDIASUBTYPE MPEG2 \_

PIN de entrada de subimagen:<br/>

-   MEDIATYPE \_ \_ paquete cifrado \_ de DVD, MEDIASUBTYPE \_ DVD \_ subpicture

A partir de Windows 7, el PIN de entrada de vídeo también admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ avc1**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**

Para obtener más información, consulte [tipos de vídeo H. 264](h-264-video-types.md) . El tipo de medio de entrada puede cambiar dinámicamente entre los tipos de MPEG2 y H. 264.<br/>

Interfaces de PIN de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

PIN de salida de vídeo:

-   Vídeo de MEDIATYPE \_ , DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)
-   \_Vídeo de MEDIATYPE, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ i420 (descodificación de software o DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ NV12 (descodificación de software o DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ YUY2 (descodificación de software o DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ IMC3 (solo DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ IMC4 (solo DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ S340 (solo DXVA 2.0)
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ YV12 (solo DXVA 2.0)

PIN de salida de línea 21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

PIN de salida de la subimagen:<br/>

-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ AI44
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ ARGB32
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ ARGB4444
-   \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ AYUV

Interfaces de clavija de salida

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo PIN de salida de vídeo)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

Identificador CLSID

**CLSID \_ de CMPEG2VidDecoderDS** (definido en wmcodecdsp. h)

Executable

msmpeg2vdec.dll

[Fundament](merit.md)

**Mérito \_ NORMAL** -1

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro tiene dos clavijas de entrada y tres clavijas de salida.

Clavijas de entrada:

-   Entrada de vídeo
-   Entrada de subimagen

Clavijas de salida:

-   Salida de vídeo
-   Salida de line-21
-   Salida de la subimagen

El filtro no crea el PIN de salida de la subimagen a menos que la clavija de entrada de vídeo esté conectada con un tipo de medio de **\_ \_ \_ paquete cifrado de DVD de MEDIATYPE** .

### <a name="mpeg-12-support"></a>Compatibilidad con MPEG-1/2

En MPEG-1 y MPEG-2, el descodificador admite los siguientes formatos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Perfiles/niveles</td>
<td>Cualquier combinación de los siguientes perfiles y niveles:<br/>
<ul>
<li>Perfiles: simple, principal</li>
<li>Niveles: bajo, principal, alto y alto 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Formatos de croma</td>
<td>croma 4:2:0</td>
</tr>
<tr class="odd">
<td>Resolución máxima</td>
<td>1920 × 1088 píxeles</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>El descodificador admite DirectX video Acceleration (DXVA) versión 1 y versión 2.</td>
</tr>
</tbody>
</table>



 

El descodificador no admite bitstreams escalables. La entrada debe ser una secuencia de vídeo elemental.

El descodificador no admite formatos de croma de 4:2:2.

### <a name="h264-support"></a>Compatibilidad con H. 264

Para H. 264, el descodificador admite los siguientes formatos:



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfiles/niveles    | Perfiles de línea base, principal y alto, hasta el nivel 5,1. (Consulte Especificación de ITU-T H. 264 para más información).                                                                                                                                                                          |
| Formatos de croma     | 4:2:0 croma o monocromo                                                                                                                                                                                                                                                |
| Resolución mínima | 48 × 48 píxeles                                                                                                                                                                                                                                                            |
| Resolución máxima | 1920 × 1088 píxeles                                                                                                                                                                                                                                                        |
| DXVA               | El descodificador admite DXVA versión 2, pero no la versión 1 de DXVA. La descodificación de DXVA solo se admite para la bitstreams de línea de base, principal y de perfil alto compatible con Main. (Las bitstreams de línea de base compatibles con Main se definen como el **perfil \_ idc**= 66 y la **\_ \_ marca de Set1 restringida**= 1). |



 

El descodificador no admite la tecnología de grano de películas.

Para obtener información sobre los tipos de medios H. 264, consulte [tipos de vídeo h. 264](h-264-video-types.md).

### <a name="codec-properties"></a>Propiedades de códec

Los pin de entrada admiten los siguientes conjuntos de propiedades a través de [**IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades de subimagen de DVD**](dvd-subpicture-property-set.md) (solo PIN de subimagen)

Los pin de entrada admiten las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                  | Requiere      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                                | Requiere      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de DVD**](dvd-media-types.md)
</dt> <dt>

[Tipos de vídeo H. 264](h-264-video-types.md)
</dt> </dl>

 

 
