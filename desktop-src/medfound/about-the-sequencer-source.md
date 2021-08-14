---
description: Acerca del origen del secuenciador
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Acerca del origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d81799a8bc1e46ade10989bbe485c69e839832fce0ded14220c536809e23e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065568"
---
# <a name="about-the-sequencer-source"></a>Acerca del origen del secuenciador

El origen del secuenciador permite a [](media-sources.md) una aplicación reproducir una colección de orígenes multimedia secuencialmente, con transiciones sin problemas entre los orígenes. El origen del secuenciador se puede usar para los escenarios siguientes:

-   Cree una lista de reproducción que cambia sin problemas de un origen multimedia al siguiente.
-   Reproducir secuencias de varios orígenes simultáneamente; por ejemplo, reproducir el audio de un archivo con el vídeo de otro.
-   Cambiar entre secuencias de diferentes orígenes multimedia en entradas consecutivas de lista de reproducción; Por ejemplo, una lista de reproducción puede tener entradas que comparten el mismo origen de vídeo, mientras que cada entrada contiene un origen de audio diferente.

Para cada elemento de una lista de reproducción, la aplicación crea una topología independiente. Los orígenes multimedia de estas topologías se conocen como *orígenes* nativos para distinguirlos del origen del secuenciador. Durante la reproducción, toda la secuencia de topologías se denomina presentación *y* cada topología dentro de la secuencia se denomina *segmento*.

La reproducción se controla mediante [la sesión multimedia,](media-session.md)que proporciona controles de transporte, como reproducir, pausar y detener. La sesión multimedia también administra el tiempo de presentación y envía eventos a la aplicación. (Los eventos del origen del secuenciador se reenvía a la aplicación a través de la sesión multimedia).

Para crear una lista de reproducción, la aplicación crea una o varias topologías de reproducción y las pone en cola en el origen del secuenciador en el orden deseado de reproducción. Internamente, el origen del secuenciador modifica las topologías para que los nodos de origen apunten al origen del secuenciador en lugar del origen nativo. La aplicación envía estas topologías modificadas, en lugar de las topologías originales, a la sesión multimedia. Esto permite que el origen del secuenciador agregue los orígenes nativos y se comunique con la sesión multimedia.

Para lograr transiciones sin problemas entre segmentos, el origen del secuenciador preinsluye cada segmento. Mientras se reproduce un segmento y antes de que sea el momento de reproducir el segmento siguiente, el origen del secuenciador activa un evento [MENewPresentation](menewpresentation.md) que contiene un descriptor de presentación. La aplicación usa este descriptor de presentación para obtener la topología para el siguiente segmento de la presentación y pone en cola la topología en la sesión multimedia.

En la ilustración siguiente se muestra el flujo de datos de las entradas de lista de reproducción a través del origen del secuenciador. La aplicación usa el solucionador de origen para crear los orígenes nativos, compila topologías para cada segmento y pone en cola las topologías en el origen del secuenciador.

![diagrama en el que se muestra el flujo de datos de los segmentos imfmediasession, imfsequencersource y playlist que conduce a imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear una lista de reproducción](how-to-create-a-playlist.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> <dt>

[Usar el origen del secuenciador](using-the-sequencer-source.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



