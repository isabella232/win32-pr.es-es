---
description: Orígenes en directo
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Orígenes en directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495065"
---
# <a name="live-sources"></a>Orígenes en directo

Un origen en directo, también denominado *origen* de la extracción, recibe datos en tiempo real. Algunos ejemplos son captura de vídeo y difusión de red. En general, un origen en directo no puede controlar la velocidad a la que llegan los datos.

Se considera que un filtro es un origen en directo si se cumple alguna de las siguientes condiciones:

-   El filtro devuelve la \_ marca AM Filter \_ Misc \_ Flags \_ es \_ Source del método [**IAMFilterMiscFlags:: GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) y al menos uno de sus clavijas de salida expone la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) .
-   El filtro expone la interfaz de [**IKsPropertySet**](ikspropertyset.md) y tiene un PIN de captura ( \_ captura de categoría de PIN \_ ). Consulte [conjunto de propiedades de PIN](pin-property-set.md) para obtener más información.

Si un filtro de origen activo proporciona un reloj, el administrador de gráficos de filtros preferirá ese reloj cuando elija el reloj de referencia del gráfico. Consulte [relojes de referencia](reference-clocks.md) para obtener más información.

**Latency**

La latencia de un filtro es la cantidad de tiempo que tarda el filtro en procesar un ejemplo. En el caso de los orígenes en directo, la latencia viene determinada por el tamaño del búfer usado para contener ejemplos. Por ejemplo, supongamos que el gráfico de filtros tiene un origen de vídeo con una latencia de 33 milisegundos (MS) y un origen de audio con una latencia de 500 ms. Cada fotograma de vídeo llega al representador de vídeo aproximadamente 470 MS antes de que el ejemplo de audio correspondiente llegue al representador de audio. A menos que el gráfico compense la diferencia, el audio y el vídeo no se sincronizarán.

Los orígenes en directo se pueden sincronizar a través de la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . El administrador de gráficos de filtro no sincroniza los orígenes en directo a menos que la aplicación habilite la sincronización llamando al método [**IAMGraphStreams:: SyncUsingStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) . Si está habilitada la sincronización, el administrador de gráficos de filtros consulta cada filtro de origen de **IAMPushSource**. Si el filtro admite **IAMPushSource**, el administrador de gráficos de filtros llama a [**IAMLatency:: GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) para recuperar la latencia esperada del filtro. (La interfaz **IAMPushSource** hereda [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency)). A partir de los valores de latencia combinada, el administrador de gráficos de filtro determina la latencia máxima esperada en el gráfico. Después llama a [**IAMPushSource:: SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) para dar a cada filtro de origen un desplazamiento de flujo, que ese filtro agrega a las marcas de tiempo que genera.

Este método está pensado principalmente para la vista previa dinámica. Sin embargo, tenga en cuenta que un PIN de vista previa en un dispositivo de captura en directo (por ejemplo, una cámara) no establece marcas de tiempo en los ejemplos que entrega. Por lo tanto, para usar este método con un dispositivo de captura en directo, debe obtener una vista previa del PIN de captura. Para obtener más información, consulte [filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md).

Actualmente, la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) es compatible con el filtro de [captura VFW](vfw-capture-filter.md) y el filtro de [captura de audio](audio-capture-filter.md) .

**Coincidencia de velocidad**

Si un filtro de representador programa ejemplos con un reloj de referencia, pero el filtro de origen los genera mediante un reloj diferente, pueden producirse problemas en la reproducción. El representador puede ejecutarse más rápido que el origen, lo que provoca huecos en los datos. O podría ejecutarse más lentamente que el origen, lo que provocaría que los ejemplos se prohicieran, hasta el momento en el que el gráfico quitará los ejemplos. Normalmente, un origen en directo no puede controlar su tasa de producción, por lo que el representador debe coincidir con las tarifas del origen.

Actualmente, solo el procesador de audio realiza la búsqueda de coincidencias, ya que los problemas de reproducción de audio son más evidentes que los problemas de vídeo. Para realizar la coincidencia de velocidad, el representador de audio debe seleccionar algo con el que coincidirá con las tarifas. Usa el algoritmo siguiente:

-   Si el gráfico no usa un reloj de referencia, el representador de audio no intenta coincidir con las tasas. (Cada vez que el gráfico no tiene ningún reloj de referencia, los ejemplos siempre se representan inmediatamente a medida que llegan).
-   De lo contrario, si hay un reloj de referencia para el gráfico, el representador de audio comprueba si hay un flujo ascendente de origen en directo, mediante los criterios descritos anteriormente. En caso contrario, el representador de audio no coincide con las tasas.
-   Si hay una conexión ascendente de origen en directo y ese origen expone la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) en su PIN de salida, el representador de audio llama a [**IAMPushSource:: GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Busca una de las marcas siguientes:
    -   \_PUSHSOURCECAPS a \_ . m \_ . Esta marca significa que el filtro de origen tiene su propio mecanismo de coincidencia de velocidad, por lo que el representador de audio no coincide con las tasas.
    -   AM \_ PUSHSOURCECAPS \_ not \_ Live. Esta marca significa que el filtro de origen no es realmente un origen en directo, aunque expone la interfaz [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Por lo tanto, el representador de audio no coincide con las tasas.
    -   \_ \_ reloj privado PUSHSOURCECAPS \_ . Esta marca significa que el filtro de origen usa un reloj privado para generar marcas de tiempo. En este caso, el representador de audio coincide con las tasas de las marcas de tiempo. (Si los ejemplos no tienen marcas de tiempo, sin embargo, el representador omite este marcador).
-   Si [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) no devuelve marcas (cero), el comportamiento del representador de audio depende del reloj del gráfico y de si los ejemplos tienen marcas de tiempo:
    -   Si el procesador de audio no es el reloj del gráfico y los ejemplos tienen marcas de tiempo, el representador de audio coincide con las tasas de las marcas de tiempo.
    -   Si los ejemplos no tienen marcas de tiempo, el procesador de audio intenta coincidir con la velocidad de los datos de audio entrantes.
    -   Si el procesador de audio es el reloj del gráfico, intenta coincidir con la velocidad de datos de entrada.

El motivo del último caso es el siguiente: Si el procesador de audio es el reloj de referencia, y el filtro de origen usa el mismo reloj para generar marcas de tiempo, el representador de audio no puede coincidir con las tasas de las marcas de tiempo. Si lo hiciera, en efecto sería intentar hacer coincidir las tasas con sí misma, lo que podría provocar que el reloj se desplazara. Por lo tanto, en este caso, el representador coincide con la tasa de datos de audio entrantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



