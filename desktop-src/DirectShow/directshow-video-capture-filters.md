---
description: Filtros de captura de vídeo de DirectShow
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: Filtros de captura de vídeo de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494410"
---
# <a name="directshow-video-capture-filters"></a>Filtros de captura de vídeo de DirectShow

Los filtros de captura en DirectShow tienen algunas características que los distinguen de otros tipos de filtros. Aunque el [generador de gráficos de captura](capture-graph-builder.md) oculta muchos de los detalles, es una buena idea leer esta sección, con el fin de tener conocimientos generales sobre los gráficos de captura de DirectShow.

**Anclar categorías**

Un filtro de captura suele tener dos o más clavijas de salida que proporcionan el mismo tipo de datos, por ejemplo, un PIN de vista previa y un PIN de captura. Por lo tanto, los tipos de medios no son una buena manera de distinguir los pin. En su lugar, las clavijas se distinguen por su funcionalidad, que se identifica mediante un GUID, denominada *categoría PIN*.

Para obtener una explicación sobre cómo consultar los pin de su categoría, consulte [trabajar con categorías de PIN](working-with-pin-categories.md). Sin embargo, para la mayoría de las aplicaciones, no tendrá que consultar directamente las clavijas. En su lugar, varios métodos [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) toman parámetros que especifican la categoría de PIN en la que se va a operar. El generador de gráficos de captura localiza automáticamente el PIN correcto.

**PIN de vista previa y clavijas de captura**

Algunos dispositivos de captura de vídeo tienen clavijas de salida independientes para la vista previa y la captura. El PIN de vista previa se usa para representar el vídeo en la pantalla, mientras que el PIN de captura se usa para escribir vídeo en un archivo.

Un PIN de vista previa y un PIN de captura tienen las siguientes diferencias:

-   Un PIN de vista previa quita los fotogramas según sea necesario para mantener el rendimiento en el PIN de captura.
-   Cada fotograma de un PIN de captura tiene una marca de tiempo con el tiempo de flujo cuando se capturó el fotograma. Un PIN de vista previa no realiza la marca de tiempo de los ejemplos que entrega.

La razón por la que los marcos de vista previa no tienen marcas de tiempo es que el gráfico de filtro introduce una pequeña cantidad de latencia en la secuencia. Si se usa la hora de captura como el tiempo de presentación, el representador de vídeo trata cada muestra como ligeramente más atrasada. Esto puede hacer que el representador de vídeo Coloque fotogramas mientras intenta ponerse al día. Al quitar las marcas de tiempo, se asegura de que el representador presenta cada ejemplo cuando llega, sin quitar fotogramas.

La categoría de PIN para los pin de vista previa es PIN \_ categoría \_ vista previa. La categoría de las clavijas de captura es la captura de categoría de PIN \_ \_ .

**PIN de puerto de vídeo**

Un puerto de vídeo es una conexión de hardware entre un dispositivo de vídeo (por ejemplo, un sintonizador de TV analógico) y la tarjeta de vídeo. Un puerto de vídeo permite que el dispositivo envíe datos de vídeo directamente a la tarjeta gráfica. El vídeo se muestra en la pantalla con una superposición de hardware. Un puerto de vídeo puede ser un cable real que conecta dos dispositivos en tarjetas independientes; o bien, podría ser una conexión cableada en la misma tarjeta.

La ventaja de un puerto de vídeo es que el vídeo se dirige directamente a la memoria de vídeo, sin ningún trabajo de la CPU. Sin embargo, los puertos de vídeo tienen algunas desventajas:

-   Un puerto de vídeo siempre usa la superficie de superposición durante la captura, independientemente de si desea obtener una vista previa del vídeo.
-   El volteo entre fotogramas se produce automáticamente, lo que dificulta la sincronización del volteo con otras operaciones de vídeo.

Si un dispositivo de captura usa un puerto de vídeo, el filtro de captura tiene un PIN de puerto de vídeo en lugar de un PIN de vista previa. La categoría PIN de los PIN del puerto de vídeo es el puerto de videojuego \_ categoría \_ .

Cada filtro de captura tiene al menos un PIN de captura. Además, podría tener un PIN de vista previa o un PIN de puerto de vídeo, pero nunca ambos. Los filtros pueden tener varias clavijas de captura y versiones preliminares, cada una de las cuales proporciona un tipo de medio independiente. Por lo tanto, un solo filtro podría tener un PIN de captura de vídeo, un PIN de vista previa de vídeo, un PIN de captura de audio y un PIN de vista previa de audio. Sin embargo, no hay nada equivalente a un puerto de vídeo para audio.

**Filtros WDM ascendentes**

Es posible que los dispositivos Modelo de controlador de Windows (WDM) requieran algunos filtros adicionales ascendentes desde el filtro de captura. Estos filtros incluyen los siguientes:

-   [Filtro de sintonizador de TV](tv-tuner-filter.md). Controla la optimización de sintonizadores de TV analógicas.
-   [Filtro de audio de TV](tv-audio-filter.md). Controla la configuración de audio para sintonizadores de TV analógicos.
-   [Filtro de barras de vídeos analógicos](analog-video-crossbar-filter.md). Enruta las señales de vídeo y audio a través del dispositivo de hardware. Por ejemplo, un dispositivo puede tener varias entradas, como S-video y vídeo compuesto. El filtro de barras cruzadas permite a la aplicación seleccionar la entrada.

Aunque se trata de filtros independientes en DirectShow, normalmente representan el mismo dispositivo de hardware. Cada filtro controla una función diferente del dispositivo. Los filtros están conectados mediante PIN, pero no se mueven datos multimedia a través de las conexiones del PIN. Por lo tanto, los pin de estos filtros no se conectan estableciendo un tipo de medio. En su lugar, usan valores GUID denominados *medios*. Los GUID de medio se definen de forma única para un minicontrolador de dispositivo determinado. Por ejemplo, el filtro de sintonizador de TV y el filtro de captura de vídeo para la misma tarjeta de TV admiten el mismo medio, lo que permite a la aplicación crear el gráfico correctamente.

En la práctica, siempre que use **ICaptureGraphBuilder2** para compilar los gráficos de captura, estos filtros se agregan automáticamente al gráfico. Para obtener una explicación más detallada, consulte [filtros de controlador de clase WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



