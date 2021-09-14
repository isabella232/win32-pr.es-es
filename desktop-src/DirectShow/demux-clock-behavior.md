---
description: Comportamiento del reloj de demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamiento del reloj de demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061232"
---
# <a name="demux-clock-behavior"></a>Comportamiento del reloj de demux

En el modo de inserción, el demultiplexador MPEG-2 (demux) expone la [**interfaz IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) Actúa como un origen en directo, por lo que se elegirá como reloj de referencia de grafo de forma predeterminada. Vea [Live Sources (Orígenes en](live-sources.md) directo) para obtener más información.

-   En el caso de las secuencias de transporte, demux sincroniza su reloj con la secuencia PCR que corresponde a la secuencia de audio o vídeo asignada más recientemente por la aplicación. Internamente, demux realiza un seguimiento de las tablas PAT y PMT. Cuando la aplicación asigna un PID de flujo elemental a un pin de salida, el demux busca la secuencia PCR para ese PID y usa esa secuencia pcr. (Actualmente, no hay manera de que la aplicación especifique el PID de PCR directamente).
-   En el caso de las secuencias de programa, demux sincroniza su reloj con la secuencia SCR.

Sincronizar el reloj de filtro con el flujo DE PCR o SCR evita el desbordamiento de datos o el subdesbordamiento, lo que podría producirse si el reloj del gráfico variaba desde el reloj de la secuencia. Demux también traduce los valores PES PTS DirectShow tiempos de referencia y usa estos valores para marcar el tiempo de los ejemplos multimedia. Las marcas de tiempo se aplican al límite del fotograma siguiente; no hay ninguna garantía de que el límite del marco se alineará con el inicio del ejemplo multimedia.

La demux garantiza que las marcas de tiempo aumenten de forma monónica. Esto significa, por ejemplo, que si una secuencia de transporte incluye un segmento como un comercial que se creó con un reloj diferente al programa principal, el demux ajustará las marcas de tiempo de presentación para ocultar la discontinuidad de tiempo de los filtros de bajada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



