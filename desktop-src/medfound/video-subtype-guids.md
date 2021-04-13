---
description: Los siguientes GUID de subtipo de vídeo se definen en el archivo de encabezado mfapi. h. Para especificar el subtipo, establezca el \_ \_ atributo de subtipo MF MT en el tipo de medio.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: GUID de subtipo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544766"
---
# <a name="video-subtype-guids"></a>GUID de subtipo de vídeo

Los siguientes GUID de subtipo de vídeo se definen en el archivo de encabezado mfapi. h. Para especificar el subtipo, establezca el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) en el tipo de medio.

Cuando se usan estos subtipos, establezca el atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) en **MFMediaType \_ video**.

-   [Formatos RGB sin comprimir](#uncompressed-rgb-formats)
-   [Formatos YUV: 8 bits y con paleta](#yuv-formats-8-bit-and-palettized)
-   [Formatos YUV: de 10 y 16 bits](#yuv-formats-10-bit-and-16-bit)
-   [Formatos de luminancia y profundidad](#luminance-and-depth-formats)
-   [Tipos de vídeo codificados](#encoded-video-types)
-   [Crear GUID de subtipos a partir de valores FOURCCs y D3DFORMAT](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Temas relacionados](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Formatos RGB sin comprimir



| GUID                             | Descripción                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ RGB8**          | RGB, 8 bits por píxel (BPP). (El mismo diseño de memoria que **D3DFMT \_ P8**).                            |
| **MFVideoFormat \_ RGB555**        | RGB 555, 16 BPP. (El mismo diseño de memoria que **D3DFMT \_ X1R5G5B5**).                                  |
| **MFVideoFormat \_ RGB565**        | RGB 565, 16 BPP. (El mismo diseño de memoria que **D3DFMT \_ R5G6B5**).                                    |
| **MFVideoFormat \_ RGB24**         | RGB, 24 BPP.                                                                                    |
| **MFVideoFormat \_ RGB32**         | RGB, 32 bpp.                                                                                    |
| **MFVideoFormat \_ ARGB32**        | RGB, 32 bpp con canal alfa.                                                                 |
| **MFVideoFormat \_ A2R10G10B10**   | RGB, 10 BPP para cada color y 2 BPP para alpha. (El mismo diseño de memoria que **D3DFMT \_ A2B10G10R10**) |
| **MFVideoFormat \_ A16B16G16R16F** | RGB, 16 BPP con canal alfa. (El mismo diseño de memoria que **D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Estos subtipos no coinciden con los GUID de subtipo RGB utilizados en los SDK anteriores, como DirectShow.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>Formatos YUV: 8 bits y con paleta



| GUID                    | Formato | muestreo | Empaquetado o plano | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ AI44** | AI44   | 4:4:4    | Equipado           | Paleta       |
| **MFVideoFormat \_ AYUV** | AYUV   | 4:4:4    | Equipado           | 8                |
| **MFVideoFormat \_ i420** | I420   | 4:2:0    | Trayectoria           | 8                |
| **MFVideoFormat \_ IYUV** | IYUV   | 4:2:0    | Trayectoria           | 8                |
| **MFVideoFormat \_ NV11** | NV11   | 4:1:1    | Trayectoria           | 8                |
| **MFVideoFormat \_ NV12** | NV12   | 4:2:0    | Trayectoria           | 8                |
| **MFVideoFormat \_ UYVY** | UYVY   | 4:2:2    | Equipado           | 8                |
| **MFVideoFormat \_ Y41P** | Y41P   | 4:1:1    | Equipado           | 8                |
| **MFVideoFormat \_ Y41T** | Y41T   | 4:1:1    | Equipado           | 8                |
| **MFVideoFormat \_ Y42T** | Y42T   | 4:2:2    | Equipado           | 8                |
| **MFVideoFormat \_ YUY2** | YUY2   | 4:2:2    | Equipado           | 8                |
| **MFVideoFormat \_ YVU9** | YVU9   | 8:4:4    | Trayectoria           | 9                |
| **MFVideoFormat \_ YV12** | YV12   | 4:2:0    | Trayectoria           | 8                |
| **MFVideoFormat \_ YVYU** | YVYU   | 4:2:2    | Equipado           | 8                |



 

Los formatos YUV recomendados se describen en detalle en el tema [formatos YUV de 8 bits recomendados para la representación de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md).

> [!Note]  
> I420 y IYUV tienen el mismo diseño en la memoria, pero se les asignan GUID de subtipo distintos. Los GUID del subtipo corresponden a los códigos FOURCC ' i420 ' y ' IYUV '; consulte [vídeo FOURCCs](video-fourccs.md) para obtener más información.

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>Formatos YUV: de 10 y 16 bits



| GUID                    | Formato | muestreo | Empaquetado o plano | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ P010** | P010   | 4:2:0    | Trayectoria           | 10               |
| **MFVideoFormat \_ P016** | P016   | 4:2:0    | Trayectoria           | 16               |
| **MFVideoFormat \_ P210** | P210   | 4:2:2    | Trayectoria           | 10               |
| **MFVideoFormat \_ P216** | P216   | 4:2:2    | Trayectoria           | 16               |
| **MFVideoFormat \_ v210** | v210   | 4:2:2    | Equipado           | 10               |
| **MFVideoFormat \_ v216** | v216   | 4:2:2    | Equipado           | 16               |
| **MFVideoFormat \_ V410** | v40    | 4:4:4    | Equipado           | 10               |
| **MFVideoFormat \_ Y210** | Y210   | 4:2:2    | Equipado           | 10               |
| **MFVideoFormat \_ Y216** | Y216   | 4:2:2    | Equipado           | 16               |
| **MFVideoFormat \_ Y410** | Y40    | 4:4:4    | Equipado           | 10               |
| **MFVideoFormat \_ Y416** | Y416   | 4:4:4    | Equipado           | 16               |



 

Para obtener más información acerca de estos formatos, vea [formatos de vídeo YUV de 10 y 16](10-bit-and-16-bit-yuv-video-formats.md)bits.

## <a name="luminance-and-depth-formats"></a>Formatos de luminancia y profundidad



| GUID                   | Descripción                                                          |
|------------------------|----------------------------------------------------------------------|
| **MFVideoFormat \_ L8**  | solo luminancia de 8 bits. (BPP). (El mismo diseño de memoria que **D3DFMT \_ L8**). |
| **MFVideoFormat \_ L16** | solo luminancia de 16 bits. (El mismo diseño de memoria que **D3DFMT \_ L16**).      |
| **MFVideoFormat \_ D16** | profundidad de búfer z de 16 bits. (El mismo diseño de memoria que **D3DFMT \_ D16**).      |



 

## <a name="encoded-video-types"></a>Tipos de vídeo codificados



| GUID                        | FOURCC         | Descripción                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ DV25**     | 'dv25'         | DVCPRO 25 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVC**      | DVC         | Vídeo de DVC/DV.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i o 720/60P).                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVHD**     | 'dvhd'         | HD-DVCR (1125-60 o 1250-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVSD**     | 'dvsd'         | SDL-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVSL**     | 'dvsl'         | SD-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ H263**     | 'H263'         | Vídeo H. 263.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264**     | H264         | Vídeo H. 264.<br/> Los ejemplos de medios contienen datos de H. 264 fragmentada con códigos de inicio y tienen SP/PPS intercalados. Cada ejemplo contiene una imagen completa, ya sea un campo o un marco.<br/>                                                                                                       |
| **MFVideoFormat \_ H265**     | 'H265'         | H. 265 vídeo.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 \_ s** | No aplicable | Flujo básico H. 264.<br/> Este tipo de medio es el mismo que el de **MFVideoFormat \_ H264**, salvo que los ejemplos multimedia contienen un fragmentada H. 264 fragmentado. Cada ejemplo puede contener una imagen parcial; varias imágenes completas; o una o más imágenes completas más una imagen parcial.<br/>           |
| **MFVideoFormat \_ HEVC**     | HEVC         | El perfil principal de HEVC y el perfil de imagen principal.<br/> Cada ejemplo contiene una imagen completa.<br/> Se admite en Windows 8.1 y versiones posteriores. El perfil principal de HEVC y la secuencia básica de Perfil de imagen principal. <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ s** | 'HEVS'         | Este tipo de medio es el mismo que el de **MFVideoFormat \_ HEVC**, excepto que los ejemplos de medios contienen un fragmentada fragmentado HEVC. Cada ejemplo puede contener una imagen parcial; varias imágenes completas; o una o más imágenes completas más una imagen parcial.<br/> Se admite en Windows 8.1 y versiones posteriores.<br/> |
| **MFVideoFormat \_ M4S2**     | ' M 4S2 '         | Vídeo MPEG-4 parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MJPG**     | 'MJPG'         | JPEG de movimiento.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ mp43**     | 'MP43'         | Códec Microsoft MPEG 4 versión 3. Este códec ya no se admite.                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MP4**     | MP4         | Códec ISO MPEG 4 versión 1.                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ MP4V**     | MP4V         | Vídeo MPEG-4 parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | No aplicable | Vídeo MPEG-2. (Equivalente a **\_ \_ vídeo MPEG2 MEDIASUBTYPE** en DirectShow).                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ VP80**     | 'MPG1'         | Vídeo de VP8.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP90**     | 'MPG1'         | Vídeo de VP9.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ MPG1**     | 'MPG1'         | Vídeo MPEG-1.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ MSS1**     | 'MSS1'         | Códec de pantalla de Windows Media versión 1.                                                                                                                                                                                                                                                                       |
| **MFVideoFormat \_ MSS2**     | 'MSS2'         | Códec de pantalla de Windows Media Video 9.                                                                                                                                                                                                                                                                         |
| **MFVideoFormat \_ WMV1**     | 'WMV1'         | Windows Media Video códec versión 7.                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ wmv2**     | 'WMV2'         | Códec Windows Media Video 8.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ Wmv3**     | 'WMV3'         | Códec de Windows Media Video 9.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ Wvc1**     | 'WVC1'         | SMPTE 421M ("VC-1").                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ 420O**     | '420O'         | vídeo YUV 4:2:0 de 8 bits por canal.                                                                                                                                                                                                                                                                   |
| **MFVideoFormat \_ AV1**     | 'AV01'         | Vídeo de AV1.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Crear GUID de subtipos a partir de valores FOURCCs y D3DFORMAT

Los formatos de vídeo suelen estar representados por valores FOURCCs o **D3DFORMAT** . Se reserva un intervalo de GUID para representar estos valores como subtipos. Estos GUID tienen el formato `XXXXXXXX-0000-0010-8000-00AA00389B71` , donde `XXXXXXXX` es el código FourCC de 4 bytes o el valor de **D3DFORMAT** .

Si un formato de vídeo tiene un valor FOURCC o **D3DFORMAT** asociado, puede crear el GUID de subtipo correspondiente como se indica a continuación: empiece con la constante **MFVideoFormat \_ base** y reemplace la primera **DWORD** del GUID por el valor de vídeo FourCC o **D3DFORMAT** . Puede usar la macro [**definir \_ \_ GUID de MEDIATYPE**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para este propósito.

> [!Note]  
> DirectShow también utiliza este sistema para la mayoría de los subtipos de vídeo, pero no para los formatos RGB no comprimidos. Por lo tanto, los subtipos RGB de DirectShow no coinciden con los subtipos RGB de Media Foundation.

 

La enumeración **D3DFORMAT** se define en el archivo de encabezado d3d9types. h. En la tabla siguiente se muestran los formatos RGB más comunes sin comprimir y el valor de **D3DFORMAT** correspondiente.



| Formato RGB                                                              | Valor **D3DFORMAT**     |
|-------------------------------------------------------------------------|-------------------------|
| RGB de 32 bits                                                              | **D3DFMT \_ X8R8G8B8**    |
| RGB de 32 bits con canal alfa                                           | **D3DFMT \_ A8R8G8B8**    |
| RGB de 24 bits                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (RGB de 16 bits)                                                    | **D3DFMT \_ X1R5G5B5**    |
| RGB 555 con canal alfa                                              | **D3DFMT \_ A4R4G4B4**    |
| RGB 565 (RGB de 16 bits)                                                    | **D3DFMT \_ R5G6B5**      |
| RGB de 8 bits de paleta                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (32 bits RGB con canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 R10 (32 bits RGB con canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2B10G10R10** |
| solo luminancia de 8 bits.                                                   | **D3DFMT \_ L8**          |
| solo luminancia de 16 bits.                                                  | **D3DFMT \_ L16**         |
| profundidad de búfer z de 16 bits                                                   | **D3DFMT \_ D16**         |



 

Para obtener más información sobre FOURCCs, consulte el [vídeo FOURCCs](video-fourccs.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID de tipo de medio](media-type-guids.md)
</dt> <dt>

[**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 




