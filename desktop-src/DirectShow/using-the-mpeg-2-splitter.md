---
description: Usar el divisor MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Usar el divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667850"
---
# <a name="using-the-mpeg-2-splitter"></a>Usar el divisor MPEG-2

> [!Note]  
> A partir de Microsoft® Windows® XP, el filtro de divisores MPEG-2 está en desuso. En su lugar, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .

 

El filtro de divisor de MPEG-2 admite la reproducción en modo de extracción de secuencias de programas MPEG-2 que contienen al menos uno de los siguientes tipos de secuencias.

-   Vídeo MPEG-2
-   Audio MPEG-2
-   Audio Dolby AC-3 codificado tal y como se define para DVD-Video
-   LPCM (código de pulso lineal modulado) codificado de audio como definido para DVD-Video

Para obtener una lista de los tipos de medios que admite el separador MPEG-2, consulte [tipos de medios de divisor MPEG-2](mpeg-2-splitter-media-types.md).

El divisor MPEG-2 no analiza las secuencias de transporte. Use el filtro de desmultiplexador MPEG-2 para las secuencias de transporte (solo en modo de extracción).

**Marcas de tiempo**

Al reproducir secuencias de programas MPEG-2, el filtro de divisor de MPEG-2 trata la primera referencia de reloj del sistema que encuentra como el origen de la hora de cualquier flujo. Esto difiere del [separador de secuencias MPEG-1](mpeg-1-stream-splitter-filter.md), que usa marcas de tiempo de presentación. El método [**IAMParse:: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) devuelve el tiempo de reloj del sistema de secuencias (posiblemente estimado) para los datos que ha procesado.

Si el filtro de separador MPEG-2 encuentra un ejemplo de entrada con el conjunto de propiedades discontinuidad (la propiedad discontinuidad se puede establecer mediante [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) o [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), omite los datos hasta que encuentra el primer paquete de los datos y ajusta sus marcas de tiempo para que la referencia de reloj del sistema (SCR) de ese paquete se considere idéntica al tiempo de SCR antes de la discontinuidad. Si el reloj de SCR aparece para saltar hacia atrás o para avanzar por más de un segundo, (en línea con la especificación de secuencia de programa MPEG-2), también se trata como una discontinuidad del reloj y la discrepancia del reloj aparente se resta de las marcas de tiempo que se pasan a los filtros de nivel inferior.

**Selección de flujo**

Cuando se reproduce la secuencia de programa MPEG-2, se eligen la primera secuencia de vídeo y la primera secuencia de audio que se ha encontrado al atravesar el flujo de programa. Se admite un máximo de un audio y un PIN de salida de vídeo. A través de la interfaz [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , se pueden seleccionar diferentes flujos del mismo tipo hasta el número especificado por el límite de audio en el encabezado del sistema. En el caso de audio MPEG-2, se supone que las secuencias forman un intervalo contiguo a partir de la secuencia 0xC0.

**Interfaces admitidas**

El filtro de divisor de MPEG-2 admite las siguientes interfaces.

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Solo flujo de programa MPEG-2.
-   [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Solo flujo de programa MPEG-2, solo secuencias de audio.
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Incluye el modo de búsqueda de bytes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



