---
description: Filtro de codificador de vídeo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro de codificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482641"
---
# <a name="dv-video-encoder-filter"></a>Filtro de codificador de vídeo DV

Este filtro codifica una secuencia de vídeo sin comprimir en vídeo digital (DV). Proporciona una interfaz personalizada, [**IDVEnc,**](/windows/desktop/api/Strmif/nn-strmif-idvenc)para establecer la resolución y el formato de codificación.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | | Tipos de medios de pin de entrada | <ul><li>Tipo principal: MEDIATYPE_VideoThe los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | <ul><li>Tipo principal: MEDIATYPE_Video</li><li>Subtipo: MEDIASUBTYPE_dvsd</li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_DVVideoEnc | | Página de propiedades CLSID | CLSID_DVEncPropertiesPage | | Archivos ejecutables | qdv.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Comentarios

Para vídeo de 16 bits (MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE RGB565), la entrada debe ser \_ de 720 x 480 píxeles para XEL o de 720 x 576 píxeles para PAL. En el vídeo de 24 bits, no hay restricciones de tamaño en la entrada.

La salida es siempre 720 x 480 para ÁLISIS o 720 x 576 para PAL; El vídeo de 24 bits se escala para ajustarse a estas dimensiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




