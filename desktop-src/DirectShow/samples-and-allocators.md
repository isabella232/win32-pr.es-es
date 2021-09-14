---
description: Ejemplos y asignadores
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Ejemplos y asignadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255092"
---
# <a name="samples-and-allocators"></a>Ejemplos y asignadores

Cuando un pin entrega datos multimedia a otro pin, no pasa un puntero directo al búfer de memoria. En su lugar, entrega un puntero a un objeto COM que administra la memoria. Este objeto, denominado ejemplo *multimedia,* expone la [**interfaz IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) El pin receptor accede al búfer de memoria llamando a métodos **IMediaSample,** como [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**IMediaSample::GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)e [**IMediaSample::GetActualDataLength.**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)

Los ejemplos siempre viajan de bajada, desde el pin de salida al pin de entrada. En el modelo de inserción, el pin de salida entrega un ejemplo mediante una llamada a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada. El pin de entrada procesará los datos de forma sincrónica (es decir, completamente dentro del **método Receive)** o los procesará de forma asincrónica en un subproceso de trabajo. El pin de entrada puede bloquearse dentro del **método Receive,** si necesita esperar recursos.

Otro objeto COM, denominado *asignador,* es responsable de crear y administrar ejemplos multimedia. Los asignadores exponen la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) Cada vez que un filtro necesita un ejemplo multimedia con un búfer vacío, llama al método [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) que devuelve un puntero al ejemplo. Cada conexión de pin comparte un asignador. Cuando se conectan dos pines, deciden qué filtro proporcionará el asignador. Los pines también establecen propiedades en el asignador, como el número de búferes y el tamaño de cada búfer. (Para obtener más información, vea [How Filters Conectar](how-filters-connect.md) and [Nego allocators](negotiating-allocators.md).)

En la ilustración siguiente se muestran las relaciones entre el asignador, los ejemplos de medios y el filtro.

![ejemplos de medios y asignadores](images/mediasamples.png)

**Recuentos de referencias de ejemplo multimedia**

Un asignador crea un grupo finito de ejemplos. En cualquier momento, algunos ejemplos pueden estar en uso, mientras que otros están disponibles para **las llamadas a GetBuffer.** El asignador usa el recuento de referencias para realizar un seguimiento de los ejemplos. El **método GetBuffer** devuelve un ejemplo con un recuento de referencias de 1. Si el recuento de referencias va a cero, el ejemplo vuelve al grupo del asignador, donde se puede usar en la siguiente **llamada a GetBuffer.** Siempre que el recuento de referencias permanezca por encima de cero, el ejemplo no está disponible para **GetBuffer.** Si cada muestra que pertenece al asignador está en uso, el **método GetBuffer** se bloquea hasta que hay disponible una muestra.

Por ejemplo, suponga que un pin de entrada recibe un ejemplo. Si procesa el ejemplo de forma sincrónica, dentro del **método Receive,** no incrementa el recuento de referencias. Una vez que **receive** devuelve el valor, el pin de salida libera el ejemplo, el recuento de referencias va a cero y el ejemplo vuelve al grupo del asignador. Por otro lado, si la patilla de entrada procesa el ejemplo en un subproceso de trabajo, incrementa el recuento de referencias antes de salir del **método Receive.** El recuento de referencias ahora es 2. Cuando el pin de salida libera el ejemplo, el recuento pasa a 1; el ejemplo aún no vuelve al grupo. Una vez que el subproceso de trabajo se ha realizado con el ejemplo, llama **a Release** para liberar el ejemplo. Ahora el ejemplo vuelve al grupo.

Cuando un pin recibe una muestra, puede copiar los datos en otra muestra o puede modificar la muestra original y entregarla al filtro siguiente. Potencialmente, un ejemplo puede recorrer toda la longitud del gráfico, y cada filtro llama a **AddRef** **y Release** a su vez. Por lo tanto, el pin de salida nunca debe volver a usar un ejemplo después de llamar a **Receive**, porque un filtro de nivel inferior puede estar usando el ejemplo. El pin de salida siempre debe llamar **a GetBuffer** para obtener un nuevo ejemplo.

Este mecanismo reduce la cantidad de asignación de memoria, ya que los filtros vuelvan a usar los mismos búferes. También impide que los filtros escriban accidentalmente datos que no se han procesado, porque el asignador mantiene una lista de ejemplos disponibles.

Un filtro puede usar asignadores independientes para la entrada y la salida. Podría hacerlo si expande los datos de entrada (por ejemplo, descomprimiendo). Si la salida no es mayor que la entrada, un filtro podría procesar los datos en su lugar, sin copiarlos en un nuevo ejemplo. En ese caso, dos o más conexiones de pin pueden compartir un asignador.

**Confirmar y desasignar asignadores**

Cuando un filtro crea por primera vez un asignador, el asignador no ha reservado ningún búfer de memoria. En este momento, se producirá un error en las llamadas **al método GetBuffer.** Cuando se inicia el streaming, el pin de salida llama a [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit), que confirma el asignador, lo que hace que asigne memoria. Los pines ahora pueden llamar a **GetBuffer.**

Cuando se detiene el streaming, el pin llama a [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit), que desasigna el asignador. Todas las llamadas posteriores **a GetBuffer** producirán un error hasta que el asignador vuelva a estar confirmado. Además, si alguna llamada a **GetBuffer** está bloqueada actualmente a la espera de un ejemplo, devuelve inmediatamente un código de error. El **método Decommit** puede liberar o no la memoria, dependiendo de la implementación. Por ejemplo, la [**clase CMemAllocator**](cmemallocator.md) espera hasta que su método destructor libera memoria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
