---
description: Orígenes en directo
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Orígenes en directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063211"
---
# <a name="live-sources"></a>Orígenes en directo

Un origen en directo, también denominado origen *de inserción,* recibe datos en tiempo real. Algunos ejemplos son la captura de vídeo y las difusiones de red. En general, un origen en directo no puede controlar la velocidad a la que llegan los datos.

Un filtro se considera un origen en directo si se cumple alguna de las siguientes condiciones:

-   El filtro devuelve la marca MISC FLAGS IS SOURCE de AM FILTER del método \_ \_ \_ \_ \_ [**IAMFilterMiscFlags::GetMiscFlags,**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) Y al menos uno de sus marcadores de salida expone la [**interfaz IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)
-   El filtro expone la interfaz [**IKsPropertySet**](ikspropertyset.md) y tiene un pin de captura (PIN \_ CATEGORY \_ CAPTURE). Consulte [Anclar conjunto de propiedades](pin-property-set.md) para obtener más información.

Si un filtro de origen en directo proporciona un reloj, filter Graph Manager preferirá ese reloj cuando elija el reloj de referencia del gráfico. Consulte [Relojes de referencia para](reference-clocks.md) obtener más información.

**Latency**

La latencia de un filtro es la cantidad de tiempo que tarda el filtro en procesar una muestra. En el caso de los orígenes en directo, la latencia viene determinada por el tamaño del búfer utilizado para contener muestras. Por ejemplo, supongamos que el gráfico de filtros tiene un origen de vídeo con una latencia de 33 milisegundos (ms) y un origen de audio con una latencia de 500 ms. Cada fotograma de vídeo llega al representador de vídeo aproximadamente 470 ms antes de que la muestra de audio correspondiente llegue al representador de audio. A menos que el gráfico compense la diferencia, el audio y el vídeo no se sincronizarán.

Los orígenes en directo se pueden sincronizar a través de [**la interfaz IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) Filter Graph Manager no sincroniza orígenes en directo a menos que la aplicación permita la sincronización mediante una llamada al método [**IAMGraphStreams::SyncUsingStreamOffset.**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) Si la sincronización está habilitada, el administrador de Graph consulta cada filtro de origen para **IAMPushSource.** Si el filtro admite **IAMPushSource,** filter Graph Manager llama a [**IAMLatency::GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) para recuperar la latencia esperada del filtro. (La **interfaz IAMPushSource** hereda [**IAMLatency).**](/windows/desktop/api/Strmif/nn-strmif-iamlatency) A partir de los valores de latencia combinados, filter Graph Manager determina la latencia máxima esperada en el gráfico. A continuación, llama a [**IAMPushSource::SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) para proporcionar a cada filtro de origen un desplazamiento de flujo, que ese filtro agrega a las marcas de tiempo que genera.

Este método está pensado principalmente para la versión preliminar en directo. Sin embargo, tenga en cuenta que una marca de vista previa en un dispositivo de captura en vivo (por ejemplo, una cámara) no establece marcas de tiempo en los ejemplos que entrega. Por lo tanto, para usar este método con un dispositivo de captura en vivo, debe obtener una vista previa desde el pin de captura. Para obtener más información, [vea DirectShow filtros de captura de vídeo](directshow-video-capture-filters.md).

Actualmente, [**la interfaz IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) es compatible con el filtro de captura [vfw](vfw-capture-filter.md) y el [filtro de captura de](audio-capture-filter.md) audio.

**Coincidencia de velocidad**

Si un filtro de representador programa ejemplos mediante un reloj de referencia, pero el filtro de origen los genera con un reloj diferente, pueden producirse problemas en la reproducción. El representador puede ejecutarse más rápido que el origen, lo que provoca espacios en los datos. O bien, podría ejecutarse más lentamente que el origen, lo que hace que las muestras se "acomenten", hasta que, en algún momento, el grafo quitará muestras. Normalmente, un origen activo no puede controlar su tasa de producción, por lo que en su lugar el representador debe coincidir con el origen.

Actualmente, solo el representador de audio realiza la coincidencia de velocidad, ya que los problemas en la reproducción de audio son más evidentes que los problemas del vídeo. Para realizar la coincidencia de velocidad, el representador de audio debe seleccionar algo con el que coincida con las velocidades. Usa el algoritmo siguiente:

-   Si el gráfico no usa un reloj de referencia, el representador de audio no intenta coincidir con las velocidades. (Siempre que el gráfico no tiene ningún reloj de referencia, las muestras siempre se representan inmediatamente a medida que llegan).
-   De lo contrario, si hay un reloj de referencia para el gráfico, el representador de audio comprueba si hay un origen activo ascendente, con los criterios descritos anteriormente. Si no es así, el representador de audio no coincide con las velocidades.
-   Si hay un origen activo ascendente y ese origen expone la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) en su pin de salida, el representador de audio llama a [**IAMPushSource::GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Busca una de las marcas siguientes:
    -   AM \_ PUSHSOURCECAPS \_ INTERNAL \_ RM. Esta marca significa que el filtro de origen tiene su propio mecanismo de coincidencia de velocidad, por lo que el representador de audio no coincide con las velocidades.
    -   AM \_ PUSHSOURCECAPS \_ NO ESTÁ EN \_ DIRECTO. Esta marca significa que el filtro de origen no es realmente un origen en directo, aunque expone la [**interfaz IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) Por lo tanto, el representador de audio no coincide con las velocidades.
    -   RELOJ \_ PRIVADO DE AM PUSHSOURCECAPS. \_ \_ Esta marca significa que el filtro de origen usa un reloj privado para generar marcas de tiempo. En este caso, el representador de audio coincide con las velocidades con las marcas de tiempo. (Sin embargo, si los ejemplos no tienen marcas de tiempo, el representador omite esta marca).
-   Si [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) no devuelve marcas (cero), el comportamiento del representador de audio depende del reloj del gráfico y de si las muestras tienen marcas de tiempo:
    -   Si el representador de audio no es el reloj del gráfico y los ejemplos tienen marcas de tiempo, el representador de audio coincide con las tasas de las marcas de tiempo.
    -   Si los ejemplos no tienen marcas de tiempo, el representador de audio intenta coincidir con la velocidad de los datos de audio entrantes.
    -   Si el representador de audio es el reloj del gráfico, intenta coincidir con la velocidad de datos entrante.

El motivo del último caso es el siguiente: si el representador de audio es el reloj de referencia y el filtro de origen usa el mismo reloj para generar marcas de tiempo, el representador de audio no puede coincidir con las velocidades con las marcas de tiempo. De ser así, en efecto, estaría intentando coincidir las tasas con sí mismo, lo que podría hacer que el reloj se desviase. Por lo tanto, en este caso, el representador coincide con la velocidad de los datos de audio entrantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



