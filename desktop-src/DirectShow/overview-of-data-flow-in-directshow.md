---
description: Información general sobre la Flow datos en DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: Información general sobre la Flow datos en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b755b9472690913cf8a53d2c7a8575111e336e54a81835438aa8cc9e959ed5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107665"
---
# <a name="overview-of-data-flow-in-directshow"></a>Información general sobre la Flow datos en DirectShow

En esta sección se proporciona una amplia información general sobre cómo funciona el flujo de datos DirectShow. Los detalles se pueden encontrar en otras secciones de la documentación.

Los datos se mantienen en búferes, que son simplemente matrices de bytes. Cada búfer se encapsula mediante un objeto COM denominado ejemplo *multimedia*, que implementa la [**interfaz IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Los ejemplos se crean mediante otro tipo de objeto, denominado asignador, que implementa la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) Se asigna un asignador para cada conexión de pin, aunque dos o más conexiones de pin pueden compartir el mismo asignador. En la imagen siguiente se muestra este proceso.

![búferes, ejemplos y asignadores](images/dataflow.png)

Cada asignador crea un grupo de ejemplos multimedia y asigna los búferes para cada ejemplo. Cada vez que un filtro necesita rellenar un búfer con datos, solicita un ejemplo al asignador mediante una llamada a [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Si el asignador tiene ejemplos que no están actualmente en uso por otro filtro, el **método GetBuffer** devuelve inmediatamente con un puntero al ejemplo. Si todos los ejemplos del asignador están en uso, el método se bloquea hasta que hay disponible una muestra. Cuando el método devuelve una muestra, el filtro coloca los datos en el búfer, establece las marcas adecuadas en la muestra (normalmente incluida una marca de tiempo) y entrega el ejemplo de bajada.

Cuando un filtro de representador recibe una muestra, comprueba la marca de tiempo y se mantiene en la muestra hasta que el reloj de referencia del gráfico de filtros indica que se deben representar los datos. Una vez que el filtro representa los datos, libera el ejemplo. El ejemplo no vuelve al grupo de muestras del asignador hasta que el recuento de referencias de la muestra es cero, lo que significa que cada filtro ha liberado la muestra. En la imagen siguiente se muestra este proceso.

![descodificador en espera de un ejemplo multimedia gratuito](images/dataflow2.png)

El filtro ascendente podría ejecutarse delante del representador; es decir, podría rellenar los búferes más rápido de lo que el representador los consume. Aun así, los ejemplos no se representan pronto, porque el representador contiene cada una hasta su hora de presentación. Además, el filtro ascendente no sobrescribirá los búferes accidentalmente, porque **GetSample** solo devuelve muestras que no están en uso de otro modo. La cantidad por la que el filtro ascendente puede ejecutarse con antelación viene determinada por el número de muestras del grupo del asignador.

En el diagrama anterior solo se muestra un asignador, pero normalmente hay varios asignadores por secuencia. Por lo tanto, cuando el representador libera un ejemplo, puede tener un efecto en cascada. En el diagrama siguiente se muestra una situación en la que un descodificador contiene un fotograma de vídeo comprimido mientras espera a que el representador libere un ejemplo. Un filtro de analizador también está esperando a que el descodificador libere una muestra.

![dos filtros en espera de ejemplos](images/dataflow3.png)

Cuando el representador libera su ejemplo, se devuelve la llamada pendiente del descodificador **a GetBuffer.** A continuación, el descodificador puede descodificar el fotograma de vídeo comprimido y liberar el ejemplo que estaba manteniendo, lo que desbloquea la llamada **GetBuffer** pendiente del analizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



