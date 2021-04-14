---
description: Muestras y asignadores
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Muestras y asignadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552810"
---
# <a name="samples-and-allocators"></a>Muestras y asignadores

Cuando un PIN entrega datos multimedia a otro PIN, no pasa un puntero directo al búfer de memoria. En su lugar, proporciona un puntero a un objeto COM que administra la memoria. Este objeto, denominado *ejemplo multimedia*, expone la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . El PIN receptor accede al búfer de memoria llamando a métodos de **IMediaSample** , como [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**IMediaSample::FUL**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)y [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength).

Los ejemplos siempre viajan hacia abajo, desde la clavija de salida a la clavija de entrada. En el modelo de entrada, el PIN de salida proporciona una muestra llamando a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada. El PIN de entrada procesará los datos sincrónicamente (es decir, completamente dentro del método de **recepción** ) o los procesará de forma asincrónica en un subproceso de trabajo. El PIN de entrada puede bloquearse dentro del método de **recepción** , si tiene que esperar recursos.

Otro objeto COM, denominado *allocator*, es responsable de la creación y administración de los ejemplos de multimedia. Los asignadores exponen la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Cada vez que un filtro necesita un ejemplo multimedia con un búfer vacío, llama al método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , que devuelve un puntero al ejemplo. Cada conexión de PIN comparte un asignador. Cuando dos patillas se conectan, deciden qué filtro proporcionará el asignador. Los pin también establecen propiedades en el asignador, como el número de búferes y el tamaño de cada búfer. (Para obtener más información, vea [cómo los filtros conectan](how-filters-connect.md) y [negocian los asignadores](negotiating-allocators.md)).

En la ilustración siguiente se muestran las relaciones entre el asignador, los ejemplos multimedia y el filtro.

![ejemplos de medios y asignadores](images/mediasamples.png)

**Recuentos de referencias de ejemplo multimedia**

Un asignador crea un grupo finito de ejemplos. En cualquier momento, algunos ejemplos pueden estar en uso, mientras que otros están disponibles para las llamadas de **getBuffer** . El asignador utiliza el recuento de referencias para realizar un seguimiento de los ejemplos. El método **getBuffer** devuelve un ejemplo con un recuento de referencias de 1. Si el recuento de referencias llega a cero, el ejemplo vuelve al grupo del asignador, donde se puede usar en la siguiente llamada a **getBuffer** . Siempre que el recuento de referencias se mantenga por encima de cero, el ejemplo no está disponible para **getBuffer**. Si cada ejemplo que pertenece al asignador está en uso, el método **getBuffer** se bloquea hasta que haya una muestra disponible.

Por ejemplo, supongamos que un PIN de entrada recibe un ejemplo. Si procesa el ejemplo sincrónicamente, dentro del método **Receive** , no incrementa el recuento de referencias. Una vez que **Receive** devuelve, la clavija de salida libera el ejemplo, el recuento de referencias llega a cero y el ejemplo vuelve al grupo del asignador. Por otro lado, si el PIN de entrada procesa el ejemplo en un subproceso de trabajo, incrementa el recuento de referencias antes de que se abandone el método de **recepción** . Ahora, el recuento de referencias es 2. Cuando el PIN de salida libera el ejemplo, el recuento llega a 1; el ejemplo todavía no vuelve al grupo. Una vez que el subproceso de trabajo se realiza con el ejemplo, llama a **Release** para liberar el ejemplo. Ahora el ejemplo vuelve al grupo.

Cuando un PIN recibe un ejemplo, puede copiar los datos en otro ejemplo o puede modificar el ejemplo original y entregarlo al siguiente filtro. Potencialmente, un ejemplo puede viajar a la longitud completa del gráfico, y cada filtro llama a **AddRef** y **Release** a su vez. Por lo tanto, el PIN de salida nunca debe volver a usar un ejemplo después de llamar a **Receive**, ya que un filtro de nivel inferior puede estar usando el ejemplo. El PIN de salida siempre debe llamar a **getBuffer** para obtener un nuevo ejemplo.

Este mecanismo reduce la cantidad de asignación de memoria, ya que los filtros vuelven a usar los mismos búferes. También impide que los filtros escriban accidentalmente sobre los datos que no se han procesado, porque el asignador mantiene una lista de ejemplos disponibles.

Un filtro puede utilizar asignadores independientes para la entrada y la salida. Podría hacer esto si expande los datos de entrada (por ejemplo, descomprimiendo). Si el resultado no es mayor que la entrada, un filtro podría procesar los datos en su lugar, sin copiarlos en un nuevo ejemplo. En ese caso, dos o más conexiones de PIN pueden compartir un asignador.

**Confirmación y desconfirmación de asignadores**

Cuando un filtro crea primero un asignador, el asignador no ha reservado ningún búfer de memoria. En este momento, se producirá un error en todas las llamadas al método **getBuffer** . Cuando se inicia el streaming, el PIN de salida llama a [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit), que confirma el asignador, lo que hace que se asigne memoria. Ahora, los pin pueden llamar a **getBuffer**.

Cuando se detiene el streaming, el PIN llama a [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit), que anula la confirmación del asignador. Se producirá un error en todas las llamadas subsiguientes a **getBuffer** hasta que se confirme de nuevo el asignador. Además, si alguna llamada a **getBuffer** está bloqueada actualmente a la espera de un ejemplo, devolverá inmediatamente un código de error. El método de **desconfirmación** puede liberar o no la memoria, en función de la implementación. Por ejemplo, la clase [**CMemAllocator**](cmemallocator.md) espera hasta que su método de destructor libere memoria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
