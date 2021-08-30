---
description: Uso del divisor MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Uso del divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43ba5a45d20de7af5e996b8e2837971de08c0f486a880e01f9f28a45f8ab385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049555"
---
# <a name="using-the-mpeg-2-splitter"></a>Uso del divisor MPEG-2

> [!Note]  
> A partir de Microsoft® Windows® XP, el filtro divisor MPEG-2 está en desuso. Use el [demultiplexor MPEG-2 en su](mpeg-2-demultiplexer.md) lugar.

 

El filtro divisor MPEG-2 admite la reproducción en modo de extracción de secuencias de programa MPEG-2 que contienen al menos uno de los siguientes tipos de secuencias.

-   Vídeo MPEG-2
-   Audio MPEG-2
-   Audio Dolby AC-3 codificado como definido para DVD-Video
-   Audio LPCM (linear pulse code modularted) codificado según se define para DVD-Video

Para obtener una lista de los tipos de medios que admite el divisor MPEG-2, vea Mpeg-2 Splitter Media Types (Tipos de medios [divisores MPEG-2).](mpeg-2-splitter-media-types.md)

El divisor MPEG-2 no analiza los flujos de transporte. Use el filtro Demultiplexer MPEG-2 para secuencias de transporte (solo en modo de inserción).

**Marcas de tiempo**

Al reproducir secuencias de programa MPEG-2, el filtro divisor MPEG-2 trata la primera referencia de reloj del sistema que encuentra como el origen de la hora de cualquier secuencia. Esto difiere del divisor [de flujo MPEG-1,](mpeg-1-stream-splitter-filter.md)que usa marcas de tiempo de presentación. El [**método IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) devuelve la hora del reloj del sistema de secuencias (posiblemente estimada) para los datos que ha procesado.

Si el filtro divisor MPEG-2 encuentra un ejemplo de entrada con el conjunto de propiedades de discontinuidad (la propiedad discontinuidad se puede establecer mediante [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) o [**IMediaSample2::SetProperties),**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)omite los datos hasta que encuentra el primer paquete en los datos y ajusta sus marcas de tiempo para que la referencia del reloj del sistema (SCR) para ese paquete se considere idéntica a la hora de SCR antes de la discontinuidad. Si el reloj SCR parece saltar hacia atrás o saltar hacia delante más de un segundo, entonces (en línea con la especificación de secuencia del programa MPEG-2), esto también se trata como una discontinuidad del reloj y la discrepancia del reloj aparente se resta de las marcas de tiempo que se pasan a los filtros de nivel inferior.

**Selección de secuencias**

Al reproducir la secuencia del programa MPEG-2, se elige la primera secuencia de vídeo y la primera secuencia de audio que atraviesa la secuencia del programa. Se admiten hasta un pin de salida de audio y un vídeo. A través [**de la interfaz IAMStreamSelect,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) se pueden seleccionar diferentes secuencias del mismo tipo hasta el número especificado por el límite de audio en el encabezado del sistema. En el caso del audio MPEG-2, actualmente se supone que las secuencias forman un intervalo contiguo a partir de la secuencia 0xC0.

**Interfaces admitidas**

El filtro divisor MPEG-2 admite las interfaces siguientes.

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Solo secuencia de programa MPEG-2.
-   [**IAMStreamSeleccionar**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Solo secuencias de programa MPEG-2, solo secuencias de audio.
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Incluye la búsqueda en modo byte.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



