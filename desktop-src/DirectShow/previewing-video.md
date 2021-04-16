---
description: Obtener una vista previa del vídeo
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Obtener una vista previa del vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563773"
---
# <a name="previewing-video-directshow"></a>Obtener una vista previa del vídeo (DirectShow)

Para compilar un gráfico de vista previa de vídeo, llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) como se indica a continuación:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



En este ejemplo se da por supuesto lo siguiente:

-   se inicializó *pBuild* , tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).
-   para inicializar *pCap* , se crea una instancia del filtro de captura y se agrega al gráfico de filtros, como se describe en [seleccionar un dispositivo de captura](selecting-a-capture-device.md).

El primer parámetro del método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica una categoría de PIN; para un gráfico de vista previa, use **PIN \_ categoría \_ Preview**. El segundo parámetro especifica un tipo de medio, como un GUID de tipo principal. Para vídeo, use **el \_ vídeo MEDIATYPE**. Los dispositivos DV proporcionan audio y vídeo intercalados, para los que el tipo de medio es de tipo medio **\_ intercalado**. (Para obtener más información acerca de la captura de DV, consulte [vídeo digital en DirectShow](digital-video-in-directshow.md)).

El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura. Los dos parámetros siguientes no son necesarios en este ejemplo. Se usan para especificar filtros adicionales que podrían ser necesarios para representar la secuencia. Al establecer el último parámetro en **null** , el generador de gráficos de captura selecciona un representador predeterminado para la secuencia, en función del tipo de medio. En el caso de vídeo, el generador de gráficos de captura siempre usa el filtro de [representador de vídeo](video-renderer-filter.md) como representador predeterminado.

> [!Note]  
> En Windows XP y versiones posteriores, aunque el representador de mezcla de vídeo (VMR) es el representador de vídeo predeterminado para los métodos de [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , no es el representador predeterminado para el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . En cualquier plataforma, el generador de gráficos de captura siempre usa el filtro de representador de vídeo anterior, a menos que se especifique lo contrario.

 

Aunque la categoría PIN se proporciona como **\_ \_ vista previa de categoría PIN**, no importa si el filtro tiene realmente un PIN de vista previa; podría tener un PIN de puerto de vídeo o simplemente un PIN de captura. En cualquier caso, el generador de gráficos de captura crea automáticamente el gráfico correcto.

En el diagrama siguiente se muestra el gráfico más sencillo posible para obtener una vista previa del vídeo.

![gráfico de vista previa de vídeo](images/vidcap01.png)

En este diagrama, el filtro de captura tiene un PIN de vista previa, que se conecta directamente al representador de vídeo.

Si el filtro de captura solo tiene un PIN de captura, el generador de gráficos de captura inserta un filtro de forma [inteligente](smart-tee-filter.md) , que divide la secuencia en una secuencia de captura y una secuencia de vista previa. Esto se describe con más detalle en [combinación de captura de vídeo y vista previa](combining-video-capture-and-preview.md).

En algunos casos, el flujo de vídeo debe atravesar el filtro de mezclador de superposición. Si es así, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo agrega automáticamente al gráfico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de captura de vídeo y vista previa](combining-video-capture-and-preview.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



