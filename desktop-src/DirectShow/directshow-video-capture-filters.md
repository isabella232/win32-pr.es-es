---
description: DirectShow Filtros de captura de vídeo
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow Filtros de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061698"
---
# <a name="directshow-video-capture-filters"></a>DirectShow Filtros de captura de vídeo

Los filtros de DirectShow tienen algunas características que los distinguen de otros tipos de filtros. Aunque [Capture Graph Builder](capture-graph-builder.md) oculta muchos de los detalles, es una buena idea leer esta sección, con el fin de tener una comprensión general de DirectShow gráficos de captura.

**Anclar categorías**

A menudo, un filtro de captura tiene dos o más pines de salida que proporcionan el mismo tipo de datos, por ejemplo, un pin de vista previa y un pin de captura. Por lo tanto, los tipos de medios no son una buena manera de distinguir los pines. En su lugar, los pines se distinguen por su funcionalidad, que se identifica mediante un GUID, denominado categoría *de pin*.

Para obtener una explicación sobre cómo consultar los pines de su categoría, vea [Trabajar con categorías de pin.](working-with-pin-categories.md) En la mayoría de las aplicaciones, sin embargo, no tendrá que consultar los pines directamente. En su lugar, [**varios métodos ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) toman parámetros que especifican la categoría de pin en la que se va a operar. Capture Graph Builder busca automáticamente el pin correcto.

**Pins de vista previa y pins de captura**

Algunos dispositivos de captura de vídeo tienen pins de salida independientes para la versión preliminar y la captura. El pin de vista previa se usa para representar vídeo en la pantalla, mientras que el pin de captura se usa para escribir vídeo en un archivo.

Un pin de vista previa y un pin de captura tienen las siguientes diferencias:

-   Un pin de vista previa quita fotogramas según sea necesario para mantener el rendimiento en el pin de captura.
-   Cada fotograma de un pin de captura tiene una marca de tiempo con el tiempo de secuencia en que se capturó el fotograma. Una marca de vista previa no marca el tiempo de los ejemplos que entrega.

La razón por la que los fotogramas de vista previa no tienen marcas de tiempo es que el gráfico de filtros introduce una pequeña cantidad de latencia en la secuencia. Si el tiempo de captura se usa como tiempo de presentación, el representador de vídeo trata cada muestra como algo tarde. Esto puede hacer que el representador de vídeo coloque fotogramas mientras intenta ponerse al día. La eliminación de las marcas de tiempo garantiza que el representador presente cada muestra cuando llega, sin quitar fotogramas.

La categoría de pin para los pins de vista previa es PIN \_ CATEGORY \_ PREVIEW. La categoría de los pins de captura es PIN \_ CATEGORY \_ CAPTURE.

**Anclar puertos de vídeo**

Un puerto de vídeo es una conexión de hardware entre un dispositivo de vídeo (por ejemplo, un afinador de TV análogo) y la tarjeta de vídeo. Un puerto de vídeo permite al dispositivo enviar datos de vídeo directamente a la tarjeta gráfica. El vídeo se muestra en la pantalla mediante una superposición de hardware. Un puerto de vídeo podría ser un cable real que conecta dos dispositivos en tarjetas independientes. o puede ser una conexión cableada en la misma tarjeta.

La ventaja de un puerto de vídeo es que el vídeo va directamente a la memoria de vídeo, sin que la CPU funcione. Sin embargo, los puertos de vídeo tienen algunos inconvenientes:

-   Un puerto de vídeo siempre usa la superficie superpuesta durante la captura, independientemente de si desea obtener una vista previa del vídeo.
-   La volteo entre fotogramas se produce automáticamente, lo que dificulta la sincronización del volteo con otras operaciones de vídeo.

Si un dispositivo de captura usa un puerto de vídeo, el filtro de captura tiene un pin de puerto de vídeo en lugar de un pin de vista previa. La categoría de pin para los pines de puerto de vídeo es PIN \_ CATEGORY \_ VIDEOPORT.

Cada filtro de captura tiene al menos un pin de captura. Además, podría tener un pin de vista previa o un pin de puerto de vídeo, pero nunca ambos. Los filtros pueden tener varios pines de captura y de vista previa, cada uno de los que ofrece un tipo de medio independiente. Por lo tanto, un único filtro podría tener un pin de captura de vídeo, un pin de vista previa de vídeo, un pin de captura de audio y un pin de vista previa de audio. (Sin embargo, no hay nada equivalente a un puerto de vídeo para audio).

**Filtros WDM ascendentes**

Windows Los dispositivos del modelo de controlador (WDM) pueden requerir algunos filtros adicionales ascendentes desde el filtro de captura. Estos filtros incluyen lo siguiente:

-   [Tv Tuner Filter](tv-tuner-filter.md). Controla la optimización de los afinadores de TELEVISIÓN analógicos.
-   [Filtro de audio de TV](tv-audio-filter.md). Controla la configuración de audio de los afinadores de TV análogos.
-   [Filtro de barra cruzada de vídeo análogo.](analog-video-crossbar-filter.md) Enruta las señales de audio y vídeo a través del dispositivo de hardware. Por ejemplo, un dispositivo podría tener varias entradas, como S-Video y vídeo compuesto. El filtro de barra cruzada permite a la aplicación seleccionar la entrada.

Aunque se trata de filtros independientes en DirectShow, normalmente representan el mismo dispositivo de hardware. Cada filtro controla una función diferente del dispositivo. Los filtros se conectan mediante pines, pero no se mueven datos multimedia a través de las conexiones de pin. Por lo tanto, los pines de estos filtros no se conectan estableciendo un tipo de medio. En su lugar, usan valores GUID *denominados medios.* Los GUID medianos se definen de forma única para un minidriver de dispositivo determinado. Por ejemplo, el filtro tv tuner y el filtro de captura de vídeo de la misma tarjeta de TV admitirán el mismo medio, lo que permite que la aplicación compile el gráfico correctamente.

En la práctica, siempre que use **ICaptureGraphBuilder2** para compilar los gráficos de captura, estos filtros se agregan automáticamente al gráfico. Para obtener una explicación más detallada, vea [Filtros de controlador de clase WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



