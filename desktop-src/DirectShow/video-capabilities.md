---
description: Funcionalidades de vídeo
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Funcionalidades de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4841f5f33b39adc6bd12775e07085e14886d250cd59c988884ae7ca8a6a21b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290861"
---
# <a name="video-capabilities"></a>Funcionalidades de vídeo

El [**método IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) presenta funcionalidades de vídeo en una matriz de pares de estructuras [**\_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de CONFIGURACIÓN de [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) y VIDEO STREAM. Puede usarlo para exponer todos los formatos y resoluciones admitidos en un pin, como se describe a continuación.

Para obtener ejemplos relacionados con audio **de GetStreamCaps,** vea [Funcionalidades de audio](audio-capabilities.md).

Supongamos que la tarjeta de captura admite el formato JPEG en todas las resoluciones entre 160 x 120 píxeles y 320 x 240 píxeles, ambos incluidos. La diferencia entre las resoluciones admitidas es una en este caso porque se agrega o resta un píxel de cada resolución admitida para obtener la siguiente resolución admitida. Esta diferencia en las resoluciones admitidas se denomina granularidad.

Supongamos que la tarjeta también admite el tamaño 640 x 480. A continuación se muestra esta resolución única y el intervalo anterior de resoluciones (todos los tamaños entre 160 x 120 píxeles y 320 x 240 píxeles).

![resolución de 160 x 120 a 320 x 240 píxeles, más 640 x 480](images/strmcap1.png)

Además, supongamos que admite formato RGB de color de 24 bits con resoluciones entre 160 x 120 y 320 x 240, pero con una granularidad de 8. En la ilustración siguiente se muestran algunos de los tamaños válidos en este caso.

![resolución de 160 x 120 a 320 a 240, con granularidad = 8](images/strmcap3.png)

Para ponerlo de otro modo y enumerar más resoluciones, los siguientes están entre la lista de resoluciones válidas.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... resoluciones adicionales...
-   312 x 232
-   320 x 240

Use **GetStreamCaps** para exponer estas funcionalidades de formato de color y dimensión al ofrecer un tipo de medio de 320 x 240 JPEG (si es el tamaño predeterminado o preferido) junto con funcionalidades mínimas de 160 x 120, capacidades máximas de 320 x 240 y una granularidad de 1. El par siguiente que expone mediante **GetStreamCaps** es un tipo de medio de 640 x 480 JPEG junto con un mínimo de 640 x 480 y un máximo de 640 x 480 y una granularidad de 0. El tercer par incluye un tipo de medio de 320 x 240, RGB de 24 bits con capacidades mínimas de 160 x 120, capacidades máximas de 320 x 240 y una granularidad de 8. De este modo, puede publicar casi todos los formatos y funcionalidades que la tarjeta pueda admitir. Una aplicación que debe saber qué formatos de compresión proporciona puede obtener todos los pares y crear una lista de todos los subtipos únicos de los tipos de medios.

Un filtro obtiene sus rectángulos de origen y destino de tipo multimedia de los miembros **rcSource** y **rcTarget** de la estructura [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) respectivamente. Los filtros no tienen que admitir rectángulos de origen y de destino.

El rectángulo de recorte descrito en toda la [**documentación de IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) es el mismo que el rectángulo **rcSource** de la estructura **VIDEOINFOHEADER** para el pin de salida.

El rectángulo de salida descrito en la documentación de **IAMStreamConfig** es el mismo que los miembros **biWidth** y **biHeight** de la estructura **BITMAPINFOHEADER** del pin de salida (vea Datos DV en formato de archivo [AVI).](dv-data-in-the-avi-file-format.md)

Si el pin de salida de un filtro está conectado a un tipo de medio sin rectángulos de origen y destino, el filtro es necesario para extender la subrecta de origen del formato de entrada en la subrectangle de destino del formato de salida. La subrectangle de origen se almacena en el miembro **InputSize** de la estructura [**\_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de CONFIG de VIDEO STREAM.

Por ejemplo, considere el siguiente escenario de escenario de vídeo: la imagen de entrada está en formato RGB y tiene un tamaño de 160 x 120 píxeles. La esquina superior izquierda del rectángulo de origen está en coordenada (20,20) y su esquina inferior derecha está en (30,30). La imagen de salida está en formato MPEG con un tamaño de 320 x 240. La esquina superior izquierda del rectángulo de destino está en (0,0) y su esquina inferior derecha está en (100 100). En este caso, el filtro debe tomar una parte de 10 x 10 del mapa de bits de origen RGB de 160 x 120 y hacer que rellene el área superior de 100 x 100 de un mapa de bits de 320 x 240, dejando intacto el resto del mapa de bits de 320 x 240. En la ilustración siguiente se muestra este escenario.

![subrectangle stretching](images/strmcap4.png)

Es posible que un filtro no admita esto y que no se pueda conectar con un tipo de medio donde **rcSource** y **rcTarget** no estén vacíos.

La **estructura VIDEOINFOHEADER** expone información sobre las funcionalidades de velocidad de datos de un filtro. Por ejemplo, suponga que ha conectado la patilla de salida al siguiente filtro con un determinado tipo de medio (ya sea directamente o mediante el tipo de medio pasado por la función [**CMediaType::SetFormat).**](cmediatype-setformat.md) Mire el **miembro dwBitRate** de la estructura de formato **VIDEOINFOHEADER** de ese tipo de medio para ver a qué velocidad de datos debe comprimir el vídeo. Si multiplica el número de unidades de tiempo por fotograma en el miembro **AvgTimePerFrame** de la estructura **VIDEOINFOHEADER** por la velocidad de datos del miembro **dwBitRate** y divide por 10 000 000 (el número de unidades por segundo), puede averiguar cuántos bytes debe tener cada fotograma. Puede generar un marco de menor tamaño, pero nunca uno mayor. Para determinar la velocidad de fotogramas de un vídeo o un filtro de captura, use **AvgTimePerFrame** desde el tipo de medio de la patilla de salida.

 

 



