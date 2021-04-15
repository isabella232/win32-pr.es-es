---
description: Marcas de tiempo
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Marcas de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d2c472d7964ccad6ec8bbc87efd39b1c4cdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688733"
---
# <a name="time-stamps"></a>Marcas de tiempo

La *marca de tiempo* define las horas de inicio y finalización de un ejemplo multimedia, medida en el tiempo de la secuencia. La marca de tiempo se denomina a veces *hora de presentación*. Al leer el resto de este artículo, es importante recordar que no todos los formatos usan marcas de tiempo de la misma manera. Por ejemplo, no todos los ejemplos de MPEG tienen marca de tiempo. En los gráficos de filtros MPEG, la marca de tiempo no se aplica a cada fotograma hasta que se genera desde el descodificador.

Cuando un filtro de representador recibe un ejemplo, programa la representación en función de la marca de tiempo. Si el ejemplo llega tarde o no tiene ninguna marca de tiempo, el filtro representa el ejemplo inmediatamente. De lo contrario, el filtro espera hasta la hora de inicio del ejemplo antes de representar el ejemplo. (Espera la hora de inicio mediante una llamada al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) ).

Los filtros de origen y los filtros de analizador son responsables de establecer las marcas de tiempo correctas en los ejemplos que procesan. Utilice las siguientes directrices.

-   Reproducción de archivos: el primer ejemplo tiene una marca de tiempo con una hora de inicio de cero. Las marcas de tiempo subsiguientes se determinan por la longitud de muestra y la velocidad de reproducción, que a su vez viene determinada por el formato de archivo. El filtro que analiza el archivo es responsable de calcular las marcas de tiempo correctas (por ejemplo, el [divisor de AVI](avi-splitter-filter.md)).
-   Captura de vídeo y audio: cada muestra tiene una marca de tiempo con una hora de inicio igual a la hora de la secuencia en que se capturó, con las siguientes salvedades:
    -   Los fotogramas de vídeo de un PIN de vista previa (en lugar de un PIN de captura) no tienen marca de tiempo. Debido a la latencia del grafo, un fotograma de vídeo que se marca con el tiempo de captura siempre llegará tarde en el representador de vídeo. Esto puede hacer que el representador Quite fotogramas, en un intento de control de calidad. Para obtener información sobre el control de calidad, consulte [Administración de control de calidad](quality-control-management.md).
    -   Captura de audio: el filtro de captura de audio usa su propio conjunto de búferes, que son independientes de los usados por el controlador de audio. El controlador de audio rellena los búferes del filtro de captura a intervalos fijos. El intervalo depende del controlador, pero por lo general no es superior a 10 milisegundos. Las marcas de tiempo de las muestras de audio reflejan la hora a la que el controlador llenó los búferes del filtro de captura de audio. Estas horas pueden ser ligeramente inexactas, especialmente si la aplicación usa un tamaño de búfer muy pequeño. Sin embargo, los tiempos de los medios reflejarán con precisión el número de muestras de audio en el búfer.
-   Filtros MUX: dependiendo del formato de salida, es posible que un filtro MUX tenga que generar marcas de tiempo o no. Por ejemplo, el formato de archivo AVI usa una velocidad de fotogramas fija sin marcas de tiempo, por lo que el filtro de [AVI MUX](avi-mux-filter.md) supone que los ejemplos llegan aproximadamente en el momento adecuado. Sin embargo, si las marcas de tiempo de entrada muestran un hueco mayor de un fotograma, el MUX de AVI escribe una entrada de índice con el tamaño cero, para indicar un fotograma colocado. En la reproducción de archivos, se generan nuevas marcas de tiempo en tiempo de ejecución, como se ha descrito anteriormente.

Para establecer la marca de tiempo en un ejemplo, llame al método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

**Horas de medios**

Opcionalmente, el filtro también puede especificar una *hora de medio* para el ejemplo. En una secuencia de vídeo, el tiempo medio representa el número de marco. En una secuencia de audio, tiempo medio representa el número de muestra del paquete. Por ejemplo, si cada paquete contiene un segundo de audio 44,1 kilohercios (kHz), el primer paquete tendrá una hora de inicio del medio de cero y un tiempo de detención del medio de 44100. En una secuencia que se pueda buscar, la hora del medio siempre es relativa a la hora de inicio de la secuencia. Por ejemplo, supongamos que busca 2 segundos desde el inicio de una secuencia de vídeo de 15 fps. El primer ejemplo multimedia después de la búsqueda tiene una marca de tiempo de cero, pero un tiempo medio de 30.

Los filtros de representador y MUX pueden utilizar la hora del medio para determinar si se han quitado marcos o muestras, comprobando si hay huecos. Sin embargo, los filtros no son necesarios para establecer la hora del medio. Para establecer la hora del medio en un ejemplo, llame al método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



