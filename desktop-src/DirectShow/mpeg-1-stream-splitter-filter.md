---
description: Filtro divisor de flujo MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro divisor de flujo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6040197fbd04585d9ba04ce87b2780f539bf377f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982188"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Filtro divisor de flujo MPEG-1

Este filtro divide una secuencia del sistema MPEG-1 en sus secuencias de audio y vídeo de componentes.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_Stream<br /> Subtipos:<br /><ul><li>MEDIASUBTYPE_MPEG1System</li><li>MEDIASUBTYPE_MPEG1VideoCD</li><li>MEDIASUBTYPE_Audio</li><li>MEDIASUBTYPE_Video</li></ul>Consulte <a href="mpeg-1-media-types.md"> <strong>Tipos de medios MPEG-1.</strong></a><br /> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | Tipo principal: MEDIATYPE_Audio o MEDIATYPE_Video<br /> Subtipo: MEDIASUBTYPE_MPEG1Payload o MEDIASUBTYPE_MPEG1Packet<br /> Consulte <a href="mpeg-1-media-types.md"> <strong>Tipos de medios MPEG-1.</strong></a><br /> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| Filtrar CLSID | CLSID_MPEG1Splitter | 
| CLSID de la página de propiedades | Ninguna página de propiedades | 
| Executable | quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

Este archivo solo admite el modo de extracción [**a través de IAsyncReader;**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) no admite el modo de inserción.

Dado que el contenido MPEG-1 no está indexado, la búsqueda puede ser muy aproximada. Normalmente es bueno para una secuencia del sistema MPEG-1 de velocidad de bits fija (que normalmente es hardware generado para CD de vídeo).

El filtro admite la [**interfaz IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) para recuperar metadatos id3.

No todos los ejemplos MPEG tienen marcas de tiempo. La falta de una marca de tiempo en un ejemplo MPEG no es un error. Para los desarrolladores de filtros, esto significa que no debe devolver un código de error del método **Receive** del pin de entrada si se produce un error [**en IMediaSample::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) Si **Receive** devuelve cualquier valor distinto de S OK, hará que \_ el divisor deje de enviar muestras.

Si el archivo contiene una secuencia de vídeo, el divisor de secuencias MPEG-1 admite la búsqueda por número de fotograma. Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el Administrador de [filtros Graph con](filter-graph-manager.md) el valor TIME FORMAT **\_ \_ FRAME**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




