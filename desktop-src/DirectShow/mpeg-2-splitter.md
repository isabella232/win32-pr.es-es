---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465262"
---
# <a name="mpeg-2-splitter"></a>Divisor MPEG-2

A partir de Microsoft® Windows® XP, el filtro divisor MPEG-2 está en desuso. Use el [demultiplexor MPEG-2 en su](mpeg-2-demultiplexer.md) lugar.

En plataformas anteriores, use el divisor MPEG-2 para secuencias de programa MPEG-2 entregadas en modo de extracción que contengan al menos uno de los siguientes tipos de secuencias: vídeo MPEG-2; Audio MPEG-2; Audio AC3 codificado como definido para vídeo de DVD; o el audio PCM codificado como se define para el vídeo de DVD. Este filtro analiza las secuencias, crea un pin de salida para cada secuencia y envía los paquetes de audio o vídeo MPEG comprimidos a un filtro de descodificador MPEG-2.

En el caso de las secuencias de programa y transporte que se entregan en modo de inserción, use el [demultiplexor MPEG-2](mpeg-2-demultiplexer.md)en todas las plataformas.

> [!Note]  
> El divisor MPEG-2 no admite búsquedas precisas de fotogramas.

 




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages,</strong> <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | | Tipos de medios de pin de entrada | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | Depende del tipo de secuencia. Consulte <a href="mpeg-2-splitter-media-types.md">Tipos de medios divisores MPEG-2</a> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | Filtrar clsid | CLSID_MMSPLITTER | | Página de propiedades CLSID | No aplicable | | Archivos ejecutables | mpg2splt.ax | | <a href="merit.md">|</a> MERIT_NORMAL + 1 | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Uso del divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



