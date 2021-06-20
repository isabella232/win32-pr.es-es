---
description: En este ejemplo se crea un gráfico de vista previa de vídeo mediante el método ICaptureGraphBuilder2::RenderStream en DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Vista previa de vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406898"
---
# <a name="previewing-video-directshow"></a>Vista previa de vídeo (DirectShow)

Para crear un gráfico de vista previa de vídeo, llame al método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) como se muestra a continuación:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



En este ejemplo se da por supuesto lo siguiente:

-   *pBuild* se inicializó, como se describe en [Acerca del Generador de gráficos de captura.](about-the-capture-graph-builder.md)
-   *pCap* se inicializó mediante la creación de una instancia del filtro de captura y su adición al gráfico de filtros, como se describe en [Selección de un dispositivo de captura.](selecting-a-capture-device.md)

El primer parámetro del método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica una categoría pin; Para un gráfico de vista previa, use **PIN \_ CATEGORY \_ PREVIEW**. El segundo parámetro especifica un tipo de medio, como un GUID de tipo principal. En el caso del vídeo, use **MEDIATYPE \_ Video**. Los dispositivos DV proporcionan audio y vídeo intercalados, para los que el tipo de medio **es MEDIATYPE \_ intercalado.** (Para obtener más información sobre la captura de DV, vea [Vídeo digital en DirectShow).](digital-video-in-directshow.md)

El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura. Los dos parámetros siguientes no son necesarios en este ejemplo. Se usan para especificar filtros adicionales que podrían ser necesarios para representar la secuencia. Al establecer el último parámetro en **NULL,** Capture Graph Builder selecciona un representador predeterminado para la secuencia, en función del tipo de medio. En el caso del vídeo, Capture Graph Builder siempre usa el filtro [Representador de](video-renderer-filter.md) vídeo como representador predeterminado.

> [!Note]  
> En Windows XP y versiones posteriores, aunque el representador de mezcla de vídeo (VMR) es el representador de vídeo predeterminado para los métodos [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) no es el representador predeterminado para el [**método RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) En cualquier plataforma, Capture Graph Builder siempre usa el filtro De representador de vídeo antiguo, a menos que especifique lo contrario.

 

Aunque la categoría pin se proporciona como **PIN \_ CATEGORY \_ PREVIEW**, no importa si el filtro tiene realmente un pin de vista previa; podría tener un pin de puerto de vídeo o simplemente un pin de captura. En cualquier caso, Capture Graph Builder compila automáticamente el gráfico correcto.

En el diagrama siguiente se muestra el gráfico más sencillo posible para obtener una vista previa del vídeo.

![gráfico de vista previa de vídeo](images/vidcap01.png)

En este diagrama, el filtro de captura tiene un pin de vista previa, que se conecta directamente al representador de vídeo.

Si el filtro de captura solo tiene un pin de captura, Capture Graph Builder inserta un filtro [smart tee,](smart-tee-filter.md) que divide la secuencia en una secuencia de captura y una secuencia de vista previa. Esto se describe con más detalle en [Combinación de captura de vídeo y versión preliminar.](combining-video-capture-and-preview.md)

En algunos casos, la secuencia de vídeo debe pasar por el filtro Mezclador de superposición. Si es así, [**el método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo agrega al gráfico automáticamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de captura de vídeo y versión preliminar](combining-video-capture-and-preview.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



