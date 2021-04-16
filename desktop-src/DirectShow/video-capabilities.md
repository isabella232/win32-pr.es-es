---
description: Capacidades de vídeo
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Capacidades de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6287839b75bd5044644480c3abcc8248cc46dc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570952"
---
# <a name="video-capabilities"></a>Capacidades de vídeo

El método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) presenta funcionalidades de vídeo en una matriz de pares de estructuras de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y de [**\_ \_ \_ Cap de configuración de flujo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . Puede utilizar esto para exponer todos los formatos y las resoluciones admitidos en un PIN, tal y como se describe a continuación.

Para ver ejemplos relacionados con el audio de **GetStreamCaps**, consulte [capacidades de audio](audio-capabilities.md).

Supongamos que la tarjeta de captura admite el formato JPEG en todas las resoluciones entre 160 x 120 píxeles y 320 x 240 píxeles, ambos incluidos. La diferencia entre las resoluciones admitidas es una en este caso porque agrega o resta un píxel de cada resolución admitida para obtener la siguiente resolución admitida. Esta diferencia en las resoluciones admitidas se denomina granularidad.

Supongamos que la tarjeta también admite el tamaño 640 x 480. A continuación se muestra esta resolución única y el intervalo de resoluciones anterior (todos los tamaños entre 160 x 120 píxeles y 320 x 240 píxeles).

![resolución de 160 x 120 a 320 x 240 píxeles, más 640 x 480](images/strmcap1.png)

Además, supongamos que admite el formato RGB de color de 24 bits en resoluciones entre 160 x 120 y 320 x 240, pero con una granularidad de 8. En la ilustración siguiente se muestran algunos de los tamaños válidos en este caso.

![resolución de 160 x 120 a 320 a 240, con granularidad = 8](images/strmcap3.png)

Para colocarlo de otra manera y mostrar más soluciones, a continuación se muestran todos los elementos de la lista de resoluciones válidas.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... resoluciones adicionales...
-   312 x 232
-   320 x 240

Use **GetStreamCaps** para exponer estas capacidades de formato de color y de dimensión mediante el uso de un tipo de medio de 320 x 240 JPEG (si es su tamaño predeterminado o preferido) acoplado a las capacidades mínimas de 160 x 120, capacidad máxima de 320 x 240 y una granularidad de 1. El siguiente par que exponga mediante **GetStreamCaps** es un tipo de medio de 640 x 480 JPEG junto con un mínimo de 640 x 480 y un máximo de 640 x 480 y una granularidad de 0. El tercer par incluye un tipo de medio de 320 x 240, RGB de 24 bits con capacidades mínimas de 160 x 120, capacidad máxima de 320 x 240 y una granularidad de 8. De esta manera, puede publicar casi todos los formatos y la funcionalidad que puede admitir la tarjeta. Una aplicación que debe saber qué formatos de compresión proporciona puede obtener todos los pares y hacer una lista de todos los subtipos únicos de los tipos de medios.

Un filtro obtiene sus rectángulos de origen y de destino de tipo de medio de los miembros **rcSource** y **rcTarget** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , respectivamente. No es necesario que los filtros admitan los rectángulos de origen y de destino.

El rectángulo de recorte descrito en la documentación de [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) es el mismo que el rectángulo **rcSource** de la estructura **VIDEOINFOHEADER** para el PIN de salida.

El rectángulo de salida descrito en la documentación de **IAMStreamConfig** es el mismo que el de los miembros **biwidth** y **biheight** de la estructura **BITMAPINFOHEADER** del PIN de salida (consulte [datos de DV en el formato de archivo AVI](dv-data-in-the-avi-file-format.md)).

Si el PIN de salida de un filtro se conecta a un tipo de medio con rectángulos de origen y de destino no vacíos, se requiere el filtro para ajustar el subrectángulo de origen del formato de entrada al subrectángulo de destino del formato de salida. El subrectángulo de origen se almacena en el miembro **Inlocate** de la estructura de vídeo de configuración de la [**secuencia de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .

Por ejemplo, considere el siguiente escenario de compresor de vídeo: la imagen de entrada está en formato RGB y tiene un tamaño de 160 x 120 píxeles. La esquina superior izquierda del rectángulo de origen está en la coordenada (20, 20) y la esquina inferior derecha está en (30, 30). La imagen de salida está en formato MPEG con un tamaño de 320 x 240. La esquina superior izquierda del rectángulo de destino está en (0,0) y la esquina inferior derecha está en (100.100). En este caso, el filtro debe tomar una pieza de 10 x 10 del mapa de bits de origen RGB 160 x 120 y hacer que rellene el área de 100 x 100 superior de un mapa de bits de 320 x 240, lo que deja el resto del mapa de bits 320 x 240 sin tocar. En la ilustración siguiente se muestra este escenario.

![expansión de subrectángulos](images/strmcap4.png)

Es posible que un filtro no sea compatible con este y que pueda no conectarse con un tipo de medio en el que **rcSource** y **rcTarget** no estén vacíos.

La estructura **VIDEOINFOHEADER** expone información sobre las capacidades de velocidad de datos de un filtro. Por ejemplo, supongamos que ha conectado el PIN de salida al siguiente filtro con un tipo de medio determinado (ya sea directamente o mediante el tipo de medio pasado por la función [**CMediaType:: SetFormat**](cmediatype-setformat.md) ). Fíjese en el miembro **dwBitRate** de la estructura de formato **VIDEOINFOHEADER** de ese tipo de medio para ver qué velocidad de datos debe comprimir el vídeo. Si multiplica el número de unidades de tiempo por fotograma en el miembro **AvgTimePerFrame** de la estructura **VIDEOINFOHEADER** por la velocidad de datos del miembro **dwBitRate** y divide por 10 millones (el número de unidades por segundo), puede averiguar cuántos bytes deben ser cada fotograma. Puede generar un marco con un tamaño menor, pero nunca más grande. Para determinar la velocidad de fotogramas de un compresor de vídeo o de un filtro de captura, use **AvgTimePerFrame** en el tipo de medio del PIN de salida.

 

 



