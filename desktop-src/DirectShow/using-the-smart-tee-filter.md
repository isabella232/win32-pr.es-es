---
description: Uso del filtro de tee inteligente
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Uso del filtro de tee inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8897a93e8be7582a4acce1a2822160c58cfe1df79eb2093bd5d96bad9629b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650785"
---
# <a name="using-the-smart-tee-filter"></a>Uso del filtro de tee inteligente

Si un filtro de captura tiene pins de captura y vista previa independientes, puede capturar desde uno mientras se hace una vista previa del otro. Pero si el filtro no tiene ninguna marca de vista previa, puede hacer lo mismo si incluye el [filtro Smart Tee](smart-tee-filter.md) en el gráfico. Este filtro divide los datos del pin de captura en dos secuencias idénticas, una para la captura y otra para la versión preliminar. En el siguiente diagrama se muestra este proceso.

![gráfico de captura con filtro de tee inteligente](images/vidcap05.png)

El [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente el filtro de tee inteligente si es necesario. Sin embargo, si usa métodos **IGraphBuilder** para compilar el grafo y no **RenderStream,** es posible que tenga que insertar el filtro Smart Tee.

Antes de representar los pines en el filtro de captura, compruebe si el filtro tiene un pin de vista previa o un pin de puerto de vídeo. Si no es así, y desea obtener una vista previa, agregue el filtro Smart Tee al gráfico y conéctelo al pin de captura en el filtro de captura.

> [!Note]  
> Puede tratar un pin de puerto de vídeo (VP) como un tipo de pin de vista previa, por lo que un filtro con un pin de VP no necesita un filtro smart tee. Sin embargo, los pins de VP tienen otros requisitos especiales. Para obtener más información, vea [Anclar puertos de vídeo.](video-port-pins.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Combinación de captura de vídeo y versión preliminar](combining-video-capture-and-preview.md)
</dt> <dt>

[Trabajar con categorías de pin](working-with-pin-categories.md)
</dt> </dl>

 

 



