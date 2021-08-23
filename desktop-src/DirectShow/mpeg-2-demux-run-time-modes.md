---
description: Modos de Run-Time MPEG-2
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bffe5f58a18ae9e935985e8dae8dc340c3895bd2dc1a2a89965355832e701f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072969"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modos de Run-Time MPEG-2

El [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("demux") puede funcionar en modo de inserción o en modo de extracción. En el modo de inserción, los datos proceden de un origen en directo, como una difusión de red. En el modo de extracción, los datos proceden de un archivo local.

-   El modo de extracción está disponible Windows XP y versiones posteriores, solo para secuencias de programa. En las plataformas de nivel inferior, use el [filtro divisor MPEG-2.](mpeg-2-splitter.md)
-   El modo de inserción está disponible en todas las plataformas, tanto para secuencias de programa como para secuencias de transporte.

Por lo tanto, demux admite tres modos posibles: secuencias de programa en modo de extracción, secuencias de programa en modo de inserción y secuencias de transporte en modo de inserción. El demux determina qué modo usar en tiempo de ejecución. El modo se determina cuando se conecta el pin de entrada o cuando se configura el primer pin de salida, lo que ocurra primero:

-   Cuando se conecta el pin de entrada: en Windows XP y versiones posteriores, demux consulta el filtro ascendente para la [**interfaz IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) si el filtro ascendente expone esa interfaz, demux se configura para las secuencias de programa en modo de extracción. De lo contrario, demux usa el modo de inserción y el tipo de medio determina el tipo de secuencia (secuencia de programa o secuencia de transporte). Consulte Mpeg-2 Demultiplexer Media Types (Tipos de medios [**de demultiplexador MPEG-2)**](mpeg-2-demultiplexer-media-types.md) para obtener una lista de tipos de entrada.
-   Cuando se configura el primer pin de salida: si crea un pin de salida y lo consulta para [**IMPEG2PIDMap,**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)demux se configura para los flujos de transporte en modo de inserción. Si consulta el pin de [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), demux se configura para secuencias de programa, también en modo de inserción. Las consultas posteriores para la otra interfaz producirán un error, porque la demux no puede funcionar en dos modos a la vez.

Una vez que el demux se ha configurado para un modo determinado, permanece en ese modo. Para usar un modo diferente, debe crear una nueva instancia de demux.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



