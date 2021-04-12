---
description: Modos de Run-Time MPEG-2 Demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time MPEG-2 Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152568"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modos de Run-Time MPEG-2 Demux

El [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux") puede funcionar en modo de inserción o en modo de extracción. En el modo de extracción, los datos proceden de un origen en directo, como una difusión de red. En el modo de extracción, los datos proceden de un archivo local.

-   El modo de extracción está disponible en Windows XP y versiones posteriores, solo para secuencias de programas. En plataformas de nivel inferior, use el filtro [de divisor de MPEG-2](mpeg-2-splitter.md) .
-   El modo de inserciones está disponible en todas las plataformas, tanto para flujos de programa como para flujos de transporte.

Por lo tanto, Demux admite tres modos posibles: secuencias de programas en modo de extracción, secuencias de programa en modo de inserción y secuencias de transporte en modo de inserción. Demux determina qué modo se va a utilizar en tiempo de ejecución. El modo se determina cuando se conecta el PIN de entrada o cuando se configura el primer PIN de salida, lo que suceda primero:

-   Cuando el PIN de entrada se conecta: en Windows XP y versiones posteriores, el Demux consulta el filtro de nivel superior para la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Si el filtro de nivel superior expone esa interfaz, el Demux se configura a sí mismo para los flujos de programa en el modo de extracción. De lo contrario, el Demux usa el modo de extracción y el tipo de medio determina el tipo de secuencia (flujo de programa o secuencia de transporte). Consulte [**tipos de medios de desmultiplexado MPEG-2**](mpeg-2-demultiplexer-media-types.md) para obtener una lista de tipos de entrada.
-   Cuando se configura el primer PIN de salida: Si crea un PIN de salida y lo consulta para [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), el Demux se configura para flujos de transporte en el modo de extracción. Si consulta el PIN de [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), el Demux se configura a sí mismo para los flujos de programa, también en el modo de extracción. Se producirá un error en las consultas posteriores de la otra interfaz, ya que Demux no puede funcionar en dos modos a la vez.

Una vez que Demux se ha configurado para un modo determinado, permanece en ese modo. Para usar un modo diferente, debe crear una nueva instancia de Demux.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



