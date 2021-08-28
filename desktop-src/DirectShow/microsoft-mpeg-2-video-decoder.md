---
description: Este filtro descodifica el vídeo MPEG-1, MPEG-2, H.264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Descodificador de vídeo MPEG-2 de Microsoft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4afdd9609124ba1057f597c4b7a907654c62a321
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982198"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Descodificador de vídeo MPEG-2 de Microsoft

Este filtro descodifica el vídeo MPEG-1, MPEG-2, H.264.

> [!Note]  
> Lacoding del vídeo H.264 requiere Windows 7.

 

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 

En el Registro, el nombre descriptivo de este filtro es "Descodificador de vídeo DTV-DVD de Microsoft".



Filtrar información

Interfaces de filtro

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de medios de pin de entrada

Pin de entrada de vídeo:

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, VÍDEO DE MEDIASUBTYPE \_ MPEG2 \_
-   MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG1Payload
-   VÍDEO \_ MEDIATYPE, VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_

Pin de entrada de subpicture:<br/>

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, SUBPICTURE DE DVD MEDIASUBTYPE \_ \_

A partir Windows 7, la patilla de entrada de vídeo también admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ AVC1**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ h264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ X264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**

Consulte [H.264 Video Types (Tipos de vídeo de H.264)](h-264-video-types.md) para obtener más información. El tipo de medio de entrada puede cambiar dinámicamente entre los tipos MPEG2 y H.264.<br/>

Interfaces de pin de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**SAMPLESampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

Pin de salida de vídeo:

-   Vídeo \_ MEDIATYPE, modo \_ DXVAMPEG2 \_ A (DXVA 1.0)
-   Vídeo \_ MEDIATYPE, modo \_ DXVAMPEG2 \_ C (DXVA 1.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ I420 (Descodificación de software o DXVA2.0)
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NV12 (Descodificación de software o DXVA2.0)
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ YUY2 (Descodificación de software o DXVA2.0)
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ IMC3 (solo DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC4 (solo DXVA2.0)
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ S340 (solo DXVA2.0)
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ YV12 (solo DXVA2.0)

Pin de salida line-21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Pin de salida de subpicture:<br/>

-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ AI44
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ ARGB32
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ ARGB4444
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ AYUV

Interfaces de pin de salida

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo pin de salida de vídeo)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2VidDecoderDS** (definido en wmcodecdsp.h)

Executable

msmpeg2vdec.dll

[Mérito](merit.md)

**LUGAR DE LA CONS \_ NORMAL:** 1

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro tiene dos pines de entrada y tres de salida.

Pines de entrada:

-   Entrada de vídeo
-   Entrada de subimagen

Pins de salida:

-   Salida de vídeo
-   Salida de línea 21
-   Salida de subimagen

El filtro no crea el pin de salida de subpicture a menos que el pin de entrada de vídeo esté conectado con un tipo de medio **\_ MEDIATYPE DVD \_ ENCRYPTED \_ PACK.**

### <a name="mpeg-12-support"></a>Compatibilidad con MPEG-1/2

Para MPEG-1 y MPEG-2, el descodificador admite los siguientes formatos:




| Etiqueta | Value |
|--------|-------|
| Perfiles o niveles | Cualquier combinación de los siguientes perfiles y niveles:<br /><ul><li>Perfiles: Simple, Main</li><li>Niveles: Bajo, Principal, Alto, Alto 1440</li></ul> | 
| Formatos de los colores | 4:2:0(4:2:0) | 
| Resolución máxima | 1920 × 1088 píxeles | 
| DXVA | El descodificador admite DirectX Video Acceleration (DXVA) versión 1 y versión 2. | 




 

El descodificador no admite secuencias de bits escalables. La entrada debe ser una secuencia de vídeo elemental.

El descodificador no admite formatos de 4:2:2.

### <a name="h264-support"></a>Compatibilidad con H.264

Para H.264, el descodificador admite los siguientes formatos:



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfiles y niveles    | Perfiles de línea base, principal y alto, hasta el nivel 5.1. (Consulte la especificación ITU-T H.264 para obtener más información).                                                                                                                                                                          |
| Formatos de traslación     | 4:2:0, color azul o monocromo                                                                                                                                                                                                                                                |
| Resolución mínima | 48 × 48 píxeles                                                                                                                                                                                                                                                            |
| Resolución máxima | 1920 × 1088 píxeles                                                                                                                                                                                                                                                        |
| DXVA               | El descodificador admite DXVA versión 2, pero no DXVA versión 1. Lacoding DXVA solo se admite para las secuencias de bits de perfil principal, principal y alto. (Las secuencias de bits de línea de base compatibles con main se definen como **\_ idc** de perfil =66 y la marca **\_ set1 \_ restringida**=1). |



 

El descodificador no admite la tecnología De grano de película.

Para obtener información sobre los tipos de medios H.264, vea Tipos de vídeo [H.264](h-264-video-types.md).

### <a name="codec-properties"></a>Propiedades del códec

Los pines de entrada admiten los siguientes conjuntos de propiedades a través [**de IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades de subimagen de DVD**](dvd-subpicture-property-set.md) (solo patilla de subpicture)

Los pines de entrada admiten las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                  | Requiere      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

El filtro admite las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                                | Requiere      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate desktop apps \[ only\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de DVD**](dvd-media-types.md)
</dt> <dt>

[Tipos de vídeo H.264](h-264-video-types.md)
</dt> </dl>

 

 
