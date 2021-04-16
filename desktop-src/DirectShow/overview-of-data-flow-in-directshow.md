---
description: Información general sobre el flujo de datos en DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: Información general sobre el flujo de datos en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495448"
---
# <a name="overview-of-data-flow-in-directshow"></a>Información general sobre el flujo de datos en DirectShow

En esta sección se ofrece una amplia información general sobre cómo funciona el flujo de datos en DirectShow. Los detalles se pueden encontrar en otras secciones de la documentación de.

Los datos se almacenan en búferes, que son simplemente matrices de bytes. Cada búfer está incluido en un objeto COM denominado *ejemplo multimedia*, que implementa la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Los ejemplos se crean mediante otro tipo de objeto, denominado allocator, que implementa la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Se asigna un asignador para cada conexión de PIN, aunque dos o más conexiones de PIN pueden compartir el mismo asignador. En la imagen siguiente se ilustra este proceso.

![búferes, muestras y asignadores](images/dataflow.png)

Cada asignador crea un grupo de muestras de medios y asigna los búferes para cada ejemplo. Cada vez que un filtro necesita rellenar un búfer con datos, solicita un ejemplo del asignador mediante una llamada a [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Si el asignador tiene algún ejemplo que no está siendo utilizado por otro filtro, el método **getBuffer** vuelve inmediatamente con un puntero al ejemplo. Si todos los ejemplos del asignador están en uso, el método se bloquea hasta que haya una muestra disponible. Cuando el método devuelve un ejemplo, el filtro coloca los datos en el búfer, establece las marcas adecuadas en el ejemplo (normalmente incluida una marca de tiempo) y entrega el ejemplo de nivel inferior.

Cuando un filtro de representador recibe un ejemplo, comprueba la marca de tiempo y lo mantiene en el ejemplo hasta que el reloj de referencia del gráfico de filtro indica que se deben representar los datos. Una vez que el filtro representa los datos, libera el ejemplo. El ejemplo no vuelve al grupo de muestras del asignador hasta que el recuento de referencias del ejemplo es cero, lo que significa que cada filtro ha liberado el ejemplo. En la imagen siguiente se ilustra este proceso.

![descodificador esperando un ejemplo de medios libres](images/dataflow2.png)

El filtro de nivel superior puede ejecutarse antes que el representador; es decir, podría rellenar los búferes más rápido de lo que el representador los consume. Aun así, los ejemplos no se representarán pronto, ya que el representador los conserva hasta el momento de la presentación. Además, el filtro de nivel superior no sobrescribirá los búferes accidentalmente, porque **GetSample** solo devuelve ejemplos que, de otro modo, no se usan. El número de muestras en el grupo del asignador determina la cantidad por la que se puede ejecutar el filtro de nivel superior.

En el diagrama anterior solo se muestra un asignador, pero normalmente hay varios asignadores por secuencia. Por lo tanto, cuando el representador libera un ejemplo, puede tener un efecto en cascada. En el diagrama siguiente se muestra una situación en la que un descodificador contiene un fotograma de vídeo comprimido mientras espera a que el representador libere un ejemplo. Un filtro del analizador también está esperando a que el descodificador publique un ejemplo.

![dos filtros que esperan ejemplos](images/dataflow3.png)

Cuando el representador libera su ejemplo, la llamada pendiente del descodificador a **getBuffer** devuelve. A continuación, el descodificador puede descodificar el fotograma de vídeo comprimido y liberar el ejemplo que estaba manteniendo, lo que desbloquea la llamada de **getBuffer** pendiente del analizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



