---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df24cb6542c335253c9f78051805b5810b5df67
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988328"
---
# <a name="mpeg-2-splitter"></a>Divisor MPEG-2

A partir de Microsoft® Windows® XP, el filtro divisor MPEG-2 está en desuso. Use el [Demultiplexer MPEG-2 en su](mpeg-2-demultiplexer.md) lugar.

En plataformas anteriores, use el divisor MPEG-2 para secuencias de programa MPEG-2 entregadas en modo de extracción que contengan al menos uno de los siguientes tipos de secuencias: vídeo MPEG-2; Audio MPEG-2; Audio AC3 codificado según se define para vídeo de DVD; o el audio PCM codificado según se define para el vídeo de DVD. Este filtro analiza las secuencias, crea un pin de salida para cada secuencia y envía los paquetes de audio o vídeo MPEG comprimidos a un filtro descodificador MPEG-2.

Para los flujos de transporte y programa entregados en modo de inserción, use el [demultiplexor MPEG-2](mpeg-2-demultiplexer.md), en todas las plataformas.

> [!Note]  
> El divisor MPEG-2 no admite búsquedas precisas de fotogramas.

 




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages,</strong> <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | 
| Tipos de medios de pin de entrada | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | Depende del tipo de secuencia. Consulte <a href="mpeg-2-splitter-media-types.md">Mpeg-2 Splitter Media Types (Tipos de medios divisores MPEG-2).</a> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| Filtrar CLSID | CLSID_MMSPLITTER | 
| CLSID de la página de propiedades | No es aplicable | 
| Executable | mpg2splt.ax | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL + 1 | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Uso del divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



