---
description: Creación de un gráfico de captura de audio con vista previa
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Creación de un gráfico de captura de audio con vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103998028"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>Creación de un gráfico de captura de audio con vista previa

El gráfico de filtros descrito en [creación de un gráfico de captura de audio](creating-an-audio-capture-graph.md) realiza la captura solo, sin vista previa. Para obtener una vista previa y capturar al mismo tiempo, el gráfico de filtros debe utilizar el [filtro tee de anclaje infinito](infinite-pin-tee-filter.md). Este filtro tiene un PIN de entrada y crea tantos clavijas de salida como sea necesario. (Se inicia con un PIN de salida. Cada vez que se conecta un PIN de salida, se crea otro.) El filtro tee de anclaje infinito ofrece cada ejemplo que recibe, sin cambios, a través de todos los pin de salida.

Conecte el filtro de captura de audio a la patilla infinita tee y conecte el PIN infinito a tee y al filtro de [representador de DirectSound](directsound-renderer-filter.md). Conecte el multiplexor al escritor de archivos, como antes. En el diagrama siguiente se muestra el gráfico de filtros resultante para un archivo AVI.

![gráfico de captura de audio con vista previa](images/audio-capture-graph.png)

Dado que el representador de DirectSound es el representador de audio predeterminado, simplemente se puede llamar al método [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) en el PIN de salida de tee del PIN infinito. Filter Graph Manager usa [Intelligent Connect](intelligent-connect.md) para crear el representador, agregarlo al gráfico de filtro y conectar los pin.

> [!Note]  
> Si captura audio desde un micrófono y obtiene una vista previa de un altavoz en el mismo equipo, puede crear comentarios de audio.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



