---
description: Comportamiento del reloj de Demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamiento del reloj de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080007"
---
# <a name="demux-clock-behavior"></a>Comportamiento del reloj de Demux

En el modo de extracción, el demultiplexador MPEG-2 (Demux) expone la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) . Actúa como un origen en directo, por lo que se elegirá como el reloj de referencia del gráfico de forma predeterminada. vea [orígenes en directo](live-sources.md) para obtener más información.

-   En el caso de las secuencias de transporte, el Demux sincroniza su reloj con el flujo de PCR que corresponde a la secuencia de audio o de vídeo asignada más recientemente por la aplicación. Internamente, Demux realiza un seguimiento de las tablas PAT y PMT. Cuando la aplicación asigna un PID de flujo elemental a un terminal de salida, Demux busca el flujo de PCR para ese PID y usa ese flujo de PCR. (Actualmente, no hay forma de que la aplicación especifique el PID de PCR directamente).
-   En el caso de las secuencias de programa, Demux sincroniza su reloj con el flujo de SCR.

Sincronizar el reloj del filtro con el flujo PCR o SCR impide el desbordamiento o subdesbordamiento de los datos, lo que podría dar lugar a que el reloj del gráfico varíe desde el reloj de la secuencia. El Demux también traduce los valores PTS de PES en horas de referencia de DirectShow y usa estos valores para la marca de tiempo de los ejemplos de medios. Las marcas de tiempo se aplican al límite del marco siguiente; no hay ninguna garantía de que el límite del marco se alinee con el inicio del ejemplo multimedia.

Demux garantiza que las marcas de tiempo aumentan de una vez más. Esto significa, por ejemplo, que si una secuencia de transporte incluye un segmento como un comercial que se creó con un reloj diferente que el programa principal, el Demux ajustará las marcas de tiempo de presentación para ocultar la discontinuidad de tiempo de los filtros de nivel inferior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



