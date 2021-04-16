---
description: Acerca del origen del secuenciador
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Acerca del origen del secuenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542174"
---
# <a name="about-the-sequencer-source"></a>Acerca del origen del secuenciador

El origen del secuenciador permite a una aplicación reproducir de forma secuencial una colección de [orígenes multimedia](media-sources.md) , con transiciones perfectas entre los orígenes. El origen del secuenciador se puede usar para los escenarios siguientes:

-   Cree una lista de reproducción que se conmutará sin problemas desde un origen de medios hasta el siguiente.
-   Reproducir secuencias de varios orígenes simultáneamente; por ejemplo, reproduzca el audio de un archivo con el vídeo de otro.
-   Cambiar entre secuencias en diferentes fuentes de medios en entradas de lista de reproducción consecutivas; por ejemplo, una lista de reproducción puede tener entradas que comparten el mismo origen de vídeo, mientras que cada entrada contiene un origen de audio diferente.

Para cada elemento de una lista de reproducción, la aplicación crea una topología independiente. Los orígenes multimedia de estas topologías se conocen como *orígenes nativos* para distinguirlos del origen del secuenciador. Durante la reproducción, toda la secuencia de topologías se denomina *presentación* y cada topología de la secuencia se denomina *segmento*.

La reproducción se controla mediante la [sesión multimedia](media-session.md), que proporciona controles de transporte, como reproducir, pausar y detener. La sesión multimedia también administra el tiempo de presentación y envía eventos a la aplicación. (Los eventos del origen del secuenciador se reenvían a la aplicación a través de la sesión multimedia).

Para crear una lista de reproducción, la aplicación crea una o más topologías de reproducción y las pone en cola en el origen del secuenciador en el orden de reproducción deseado. Internamente, el origen del secuenciador modifica las topologías para que los nodos de origen señalen al origen del secuenciador en lugar de al origen nativo. La aplicación envía estas topologías modificadas, en lugar de las topologías originales, a la sesión multimedia. Esto permite que el origen del secuenciador agregue los orígenes nativos y se comunique con la sesión multimedia.

Para lograr transiciones perfectas entre segmentos, el origen del secuenciador realiza una reversión de cada segmento. Mientras se reproduce un segmento y antes de que sea el momento de reproducir el segmento siguiente, el origen del secuenciador desencadena un evento [MENewPresentation](menewpresentation.md) que contiene un descriptor de presentación. La aplicación utiliza este descriptor de presentación para obtener la topología para el siguiente segmento de la presentación y pone en cola la topología en la sesión multimedia.

En la ilustración siguiente se muestra el flujo de datos para las entradas de la lista de reproducción a través del origen del secuenciador. La aplicación utiliza la resolución de origen para crear los orígenes nativos, crea topologías para cada segmento y pone en cola las topologías en el origen del secuenciador.

![diagrama que muestra el flujo de datos desde los segmentos imfmediasession, imfsequencersource y playlist que conducen a imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

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

 

 



