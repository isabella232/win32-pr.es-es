---
description: Comportamiento del reloj de Demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamiento del reloj de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821190"
---
# <a name="demux-clock-behavior"></a>Comportamiento del reloj de Demux

En el modo de inserción, el demultiplexador MPEG-2 (demux) expone la [**interfaz IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) Actúa como un origen en directo, por lo que se elegirá como el reloj de referencia del gráfico de forma predeterminada. Vea [Orígenes en directo](live-sources.md) para obtener más información.

-   En el caso de las secuencias de transporte, demux sincroniza su reloj con la secuencia PCR que corresponde a la secuencia de audio o vídeo asignada más recientemente por la aplicación. Internamente, demux realiza un seguimiento de las tablas PAT y PMT. Cuando la aplicación asigna un PID de flujo básico a un pin de salida, demux busca la secuencia pcr para ese PID y usa esa secuencia pcr. (Actualmente, no hay manera de que la aplicación especifique el PID de PCR directamente).
-   En el caso de las secuencias de programa, demux sincroniza su reloj con la secuencia de SCR.

La sincronización del reloj de filtro con el flujo DE PCR o SCR evita el desbordamiento de datos o el subdesbordamiento, lo que podría producirse si el reloj del gráfico variase desde el reloj de la secuencia. Demux también traduce los valores de PTS de PES DirectShow tiempos de referencia y usa estos valores para marcar el tiempo de los ejemplos multimedia. Las marcas de tiempo se aplican al límite de fotograma siguiente; no hay ninguna garantía de que el límite del marco se alineará con el inicio del ejemplo multimedia.

La demux garantiza que las marcas de tiempo aumenten de forma monótona. Esto significa, por ejemplo, que si una secuencia de transporte incluye un segmento como un comercial que se creó con un reloj diferente al programa principal, el demux ajustará las marcas de tiempo de presentación para ocultar la discontinuidad de hora de los filtros de bajada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



