---
description: Los siguientes GUID de subtipo de vídeo se definen en el archivo de encabezado mfapi.h. Para especificar el subtipo, establezca el atributo MF \_ MT \_ SUBTYPE en el tipo de medio.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: GUID de subtipo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f4ea9724bb587b17efe26c9f8f2e729c839eb1
ms.sourcegitcommit: 8f5d85f95ad3de87226e739b86f814fc1e5d885b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2021
ms.locfileid: "129666669"
---
# <a name="video-subtype-guids"></a>GUID de subtipo de vídeo

Los siguientes GUID de subtipo de vídeo se definen en el archivo de encabezado mfapi.h. Para especificar el subtipo, establezca el atributo [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) en el tipo de medio.

Cuando se usen estos subtipos, establezca el atributo [MF \_ MT MAJOR \_ \_ TYPE](mf-mt-major-type-attribute.md) en **MFMediaType \_ Video**.

-   [Formatos RGB sin comprimir](#uncompressed-rgb-formats)
-   [Formatos de YUV: 8 bits y se ha tachado](#yuv-formats-8-bit-and-palettized)
-   [Formatos YUV: 10 y 16 bits](#yuv-formats-10-bit-and-16-bit)
-   [Formatos de luminosidad y profundidad](#luminance-and-depth-formats)
-   [Tipos de vídeo codificados](#encoded-video-types)
-   [Creación de GUID de subtipos a partir de valores FOURCC y D3DFORMAT](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Temas relacionados](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Formatos RGB sin comprimir



| GUID                             | Descripción                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ RGB8**          | RGB, 8 bits por píxel (bpp). (El mismo diseño de memoria **que D3DFMT \_ P8).**                            |
| **MFVideoFormat \_ RGB555**        | RGB 555, 16 bpp. (El mismo diseño de memoria **que D3DFMT \_ X1R5G5B5).**                                  |
| **MFVideoFormat \_ RGB565**        | RGB 565, 16 bpp. (El mismo diseño de memoria **que D3DFMT \_ R5G6B5).**                                    |
| **MFVideoFormat \_ RGB24**         | RGB, 24 bpp.                                                                                    |
| **MFVideoFormat \_ RGB32**         | RGB, 32 bpp.                                                                                    |
| **MFVideoFormat \_ ARGB32**        | RGB, 32 bpp con canal alfa.                                                                 |
| **MFVideoFormat \_ A2R10G10B10**   | RGB, 10 bpp para cada color y 2 bpp para alfa. (El mismo diseño de memoria **que D3DFMT \_ A2B10G10R10**) |
| **MFVideoFormat \_ A16B16G16R16F** | RGB, 16 bpp con canal alfa. (El mismo diseño de memoria **que D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Estos subtipos no coinciden con los GUID de subtipo RGB usados en los SDK anteriores, como DirectShow.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>Formatos de YUV: 8 bits y se ha tachado



| GUID                    | Formato | muestreo | Empaquetado o plano | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ AI44** | AI44   | 4:4:4    | Embalado           | Se ha desenlazado       |
| **MFVideoFormat \_ AYUV** | AYUV   | 4:4:4    | Embalado           | 8                |
| **MFVideoFormat \_ I420** | I420   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ IYUV** | IYUV   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ NV11** | NV11   | 4:1:1    | Planar           | 8                |
| **MFVideoFormat \_ NV12** | NV12   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ UYVY** | UYVY   | 4:2:2    | Embalado           | 8                |
| **MFVideoFormat \_ Y41P** | Y41P   | 4:1:1    | Embalado           | 8                |
| **MFVideoFormat \_ Y41T** | Y41T   | 4:1:1    | Embalado           | 8                |
| **MFVideoFormat \_ Y42T** | Y42T   | 4:2:2    | Embalado           | 8                |
| **MFVideoFormat \_ YUY2** | YUY2   | 4:2:2    | Embalado           | 8                |
| **MFVideoFormat \_ YVU9** | YVU9   | 8:4:4    | Planar           | 9                |
| **MFVideoFormat \_ YV12** | YV12   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ YVYU** | YVYU   | 4:2:2    | Embalado           | 8                |



 

Los formatos YUV recomendados se describen en detalle en el tema [Recommended 8-Bit YUV Formats for Video Rendering](recommended-8-bit-yuv-formats-for-video-rendering.md).

> [!Note]  
> I420 e IYUV tienen el mismo diseño en memoria, pero se les asignan GUID de subtipo distintos. Los GUID de subtipo corresponden a los códigos FOURCC "I420" e "IYUV"; Vea [Video FOURCCs (CTC de vídeo)](video-fourccs.md) para obtener más información.

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>Formatos YUV: 10 y 16 bits



| GUID                    | Formato | muestreo | Empaquetado o plano | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ P010** | P010   | 4:2:0    | Planar           | 10               |
| **MFVideoFormat \_ P016** | P016   | 4:2:0    | Planar           | 16               |
| **MFVideoFormat \_ P210** | P210   | 4:2:2    | Planar           | 10               |
| **MFVideoFormat \_ P216** | P216   | 4:2:2    | Planar           | 16               |
| **MFVideoFormat \_ v210** | v210   | 4:2:2    | Embalado           | 10               |
| **MFVideoFormat \_ v216** | v216   | 4:2:2    | Embalado           | 16               |
| **MFVideoFormat \_ v410** | v40    | 4:4:4    | Embalado           | 10               |
| **MFVideoFormat \_ Y210** | Y210   | 4:2:2    | Embalado           | 10               |
| **MFVideoFormat \_ Y216** | Y216   | 4:2:2    | Embalado           | 16               |
| **MFVideoFormat \_ Y410** | Y40    | 4:4:4    | Embalado           | 10               |
| **MFVideoFormat \_ Y416** | Y416   | 4:4:4    | Embalado           | 16               |



 

Para obtener más información sobre estos formatos, vea Formatos de vídeo YUV de [10 y 16 bits.](10-bit-and-16-bit-yuv-video-formats.md)

## <a name="luminance-and-depth-formats"></a>Formatos de luminosidad y profundidad



| GUID                   | Descripción                                                          |
|------------------------|----------------------------------------------------------------------|
| **MFVideoFormat \_ L8**  | Solo luminosidad de 8 bits. (bpp). (El mismo diseño de memoria **que D3DFMT \_ L8).** |
| **MFVideoFormat \_ L16** | Solo luminosidad de 16 bits. (El mismo diseño de memoria **que D3DFMT \_ L16).**      |
| **MFVideoFormat \_ D16** | Profundidad del búfer z de 16 bits. (El mismo diseño de memoria **que D3DFMT \_ D16).**      |



 

## <a name="encoded-video-types"></a>Tipos de vídeo codificados



| GUID                        | FOURCC         | Descripción                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ DV25**     | 'dv25'         | DVCPRO 25 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVC**      | 'dvc'         | Vídeo DVC/DV.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i o 720/60P).                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVHD**     | 'dvhd'         | HD-DVCR (1125-60 o 1250-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVSD**     | 'dvsd'         | SDL-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVSL**     | 'dvsl'         | SD-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ H263**     | 'H263'         | Vídeo de H.263.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264**     | 'H264'         | Vídeo de H.264.<br/> Los ejemplos multimedia contienen datos de secuencia de bits H.264 con códigos de inicio y tienen SPS o PPS intercalados. Cada ejemplo contiene una imagen completa, ya sea un campo o un marco.<br/>                                                                                                       |
| **MFVideoFormat \_ H265**     | 'H265'         | Vídeo de H.265.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 \_ ES** | No aplicable | Secuencia elemental H.264.<br/> Este tipo de medio es el mismo que **MFVideoFormat \_ H264,** excepto que los ejemplos de medios contienen una secuencia de bits H.264 fragmentada. Cada muestra puede contener una imagen parcial; varias imágenes completas; o una o varias imágenes completas más una imagen parcial.<br/>           |
| **MFVideoFormat \_ HEVC**     | 'HEVC'         | El perfil principal de HEVC y el perfil de imagen principal.<br/> Cada ejemplo contiene una imagen completa.<br/> Se admite en Windows 8.1 y versiones posteriores. El perfil principal de HEVC y la secuencia elemental del perfil de imagen principal. <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ ES** | 'HEVS'         | Este tipo de medio es el mismo que **MFVideoFormat \_ HEVC,** excepto que los ejemplos de medios contienen una secuencia de bits HEVC fragmentada. Cada muestra puede contener una imagen parcial; varias imágenes completas; o una o varias imágenes completas más una imagen parcial.<br/> Se admite en Windows 8.1 y versiones posteriores.<br/> |
| **MFVideoFormat \_ M4S2**     | 'M4S2'         | Vídeo MPEG-4, parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MJPG**     | 'MJPG'         | JPEG de movimiento.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ MP43**     | 'MP43'         | Códec Microsoft MPEG 4 versión 3. Este códec ya no se admite.                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MP4S**     | 'MP4S'         | Códec ISO MPEG 4 versión 1.                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ MP4V**     | 'MP4V'         | Vídeo MPEG-4, parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | No aplicable | Vídeo MPEG-2. (Equivalente a **MEDIASUBTYPE \_ MPEG2 \_ VIDEO** en DirectShow).                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ VP80**     | 'MPG1'         | Vídeo VP8.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP90**     | 'MPG1'         | Vídeo vp9.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ MPG1**     | 'MPG1'         | Vídeo MPEG-1.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ MSS1**     | 'MSS1'         | Windows Códec media Screen versión 1.                                                                                                                                                                                                                                                                       |
| **MFVideoFormat \_ MSS2**     | 'MSS2'         | Windows Códec de pantalla de Vídeo multimedia 9.                                                                                                                                                                                                                                                                         |
| **MFVideoFormat \_ WMV1**     | 'WMV1'         | Windows Códec Media Video versión 7.                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ WMV2**     | 'WMV2'         | Windows Códec Media Video 8.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WMV3**     | 'WMV3'         | Windows Códec Media Video 9.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WVC1**     | 'WVC1'         | SMPTE 421M ("VC-1").                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ 420O**     | '420O'         | Vídeo YUV 4:2:0 de 8 bits por canal plano.                                                                                                                                                                                                                                                                   |
| **MFVideoFormat \_ AV1**     | 'AV01'         | Vídeo de AV1.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Creación de GUID de subtipo a partir de valores DE FOURC y D3DFORMAT

Los formatos de vídeo suelen representarse mediante valores **FOURCCs o D3DFORMAT.** Se reserva un intervalo de GUID para representar estos valores como subtipos. Estos GUID tienen el formato , donde es el código FOURCC de `XXXXXXXX-0000-0010-8000-00AA00389B71` `XXXXXXXX` 4 bytes o el valor **D3DFORMAT.**

Si un formato de vídeo tiene un valor FOURCC o **D3DFORMAT** asociado, puede crear el GUID del subtipo correspondiente como se muestra a continuación: Comience por la constante **MFVideoFormat \_ Base** y reemplace la primera **DWORD** del GUID por el vídeo FOURCC o el valor **D3DFORMAT.** Puede usar la [**macro \_ DEFINE MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para este propósito.

> [!Note]  
> DirectShow usa este sistema para la mayoría de los subtipos de vídeo, pero no para formatos RGB sin comprimir. Por lo tanto, los subtipos RGB de DirectShow no coinciden con los subtipos RGB de Media Foundation.

 

La **enumeración D3DFORMAT** se define en el archivo de encabezado d3d9types.h. En la tabla siguiente se muestran los formatos RGB sin comprimir más comunes y el valor **D3DFORMAT** correspondiente.



| Formato RGB                                                              | **Valor D3DFORMAT**     |
|-------------------------------------------------------------------------|-------------------------|
| RGB de 32 bits                                                              | **D3DFMT \_ X8R8G8B8**    |
| RGB de 32 bits con canal alfa                                           | **D3DFMT \_ A8R8G8B8**    |
| RGB de 24 bits                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (RGB de 16 bits)                                                    | **D3DFMT \_ X1R5G5B5**    |
| RGB 555 con canal alfa                                              | **D3DFMT \_ A1R5G5B5**    |
| RGB 565 (RGB de 16 bits)                                                    | **D3DFMT \_ R5G6B5**      |
| RGB de 8 bits con tono                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (RGB de 32 bits con canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 R10 (RGB de 32 bits con canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2B10G10R10** |
| Solo luminosidad de 8 bits.                                                   | **D3DFMT \_ L8**          |
| Solo luminosidad de 16 bits.                                                  | **D3DFMT \_ L16**         |
| Profundidad del búfer z de 16 bits                                                   | **D3DFMT \_ D16**         |



 

Para obtener más información sobre los FOURCC, vea [Video FOURCCs](video-fourccs.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID de tipo de medio](media-type-guids.md)
</dt> <dt>

[**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 




