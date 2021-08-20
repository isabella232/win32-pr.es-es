---
description: Marcas de tiempo
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Marcas de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed14f0155a0bfbf209719f4aff97cbbd19501e6aa32d57e9f0c1cbb2df0964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072319"
---
# <a name="time-stamps"></a>Marcas de tiempo

La *marca de tiempo* define las horas de inicio y de fin de un ejemplo multimedia, medidas en tiempo de transmisión. La marca de tiempo a veces se denomina tiempo *de presentación.* Al leer el resto de este artículo, es importante recordar que no todos los formatos usan marcas de tiempo de la misma manera. Por ejemplo, no todos los ejemplos MPEG tienen marca de tiempo. En los gráficos de filtro MPEG, la marca de tiempo no se aplica a cada fotograma hasta que se genera desde el descodificador.

Cuando un filtro de representador recibe un ejemplo, programa la representación en función de la marca de tiempo. Si el ejemplo llega tarde o no tiene marca de tiempo, el filtro representa la muestra inmediatamente. De lo contrario, el filtro espera hasta la hora de inicio del ejemplo antes de representar el ejemplo. (Espera la hora de inicio llamando al [**método IReferenceClock::AdviseTime).**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

Los filtros de origen y los filtros de analizador son responsables de establecer las marcas de tiempo correctas en los ejemplos que procesan. Use las siguientes directrices.

-   Reproducción de archivos: el primer ejemplo tiene una marca de tiempo con una hora de inicio de cero. Las marcas de tiempo posteriores se determinan por la longitud de la muestra y la velocidad de reproducción, que a su vez viene determinada por el formato de archivo. El filtro que analiza el archivo es responsable de calcular las marcas de tiempo correctas (por ejemplo, el [divisor AVI](avi-splitter-filter.md)).
-   Captura de vídeo y audio: cada muestra tiene una marca de tiempo con una hora de inicio igual a la hora de transmisión cuando se capturó, con las advertencias siguientes:
    -   Los fotogramas de vídeo de un pin de vista previa (en lugar de un pin de captura) no tienen marca de tiempo. Debido a la latencia del grafo, un fotograma de vídeo marcado con el tiempo de captura siempre llegará tarde al representador de vídeo. Esto puede hacer que el representador coloque fotogramas, en un intento de control de calidad. Para obtener información sobre el control de calidad, vea [Administración de control de calidad.](quality-control-management.md)
    -   Captura de audio: el filtro de captura de audio usa su propio conjunto de búferes, que son independientes de los utilizados por el controlador de audio. El controlador de audio rellena los búferes del filtro de captura a intervalos fijos. El intervalo depende del controlador, pero generalmente no es superior a 10 milisegundos. Las marcas de tiempo de los ejemplos de audio reflejan la hora en que el controlador llenó los búferes del filtro de captura de audio. Estos tiempos pueden ser ligeramente imprecisos, especialmente si la aplicación usa un tamaño de búfer muy pequeño. Sin embargo, los tiempos multimedia reflejarán con precisión el número de muestras de audio en el búfer.
-   Filtros de Mux: dependiendo del formato de salida, es posible que un filtro mux tenga que generar marcas de tiempo o no. Por ejemplo, el formato de archivo AVI usa una velocidad de fotogramas fija sin marcas de tiempo, por lo que el filtro [avi Mux](avi-mux-filter.md) supone que las muestras llegan aproximadamente en el momento adecuado. Sin embargo, si las marcas de tiempo entrantes muestran un intervalo mayor que un fotograma, el Mux avi escribe una entrada de índice con el tamaño cero para indicar un fotograma eliminado. En la reproducción de archivos, se generan nuevas marcas de tiempo en tiempo de ejecución, como se describió anteriormente.

Para establecer la marca de tiempo en un ejemplo, llame al [**método IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

**Horas de medios**

Opcionalmente, el filtro también puede especificar un *tiempo multimedia* para el ejemplo. En una secuencia de vídeo, el tiempo del medio representa el número de fotograma. En una secuencia de audio, el tiempo del medio representa el número de muestra en el paquete. Por ejemplo, si cada paquete contiene un segundo de audio de 44,1 kilohercios (kHz), el primer paquete tiene una hora de inicio multimedia de cero y una hora de detención de medios de 44100. En una secuencia que se puede buscar, la hora del medio siempre es relativa a la hora de inicio de la secuencia. Por ejemplo, supongamos que busca a 2 segundos desde el inicio de una secuencia de vídeo de 15 fps. El primer ejemplo multimedia después de la búsqueda tiene una marca de tiempo de cero, pero un tiempo de medios de 30.

Los filtros de representador y mux pueden usar el tiempo de medios para determinar si se han eliminado fotogramas o muestras, comprobando si hay espacios. Sin embargo, no se necesitan filtros para establecer el tiempo de los medios. Para establecer la hora del medio en un ejemplo, llame al [**método IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



