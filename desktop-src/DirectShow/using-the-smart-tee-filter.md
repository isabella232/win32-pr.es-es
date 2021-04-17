---
description: Usar el filtro Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Usar el filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667849"
---
# <a name="using-the-smart-tee-filter"></a>Usar el filtro Smart Tee

Si un filtro de captura tiene clavijas de captura y vista previa independientes, puede capturar desde uno mientras obtiene una vista previa del otro. Pero si el filtro no tiene ningún PIN de vista previa, puede hacer lo mismo incluyendo el filtro [Smart Tee](smart-tee-filter.md) en el gráfico. Este filtro divide los datos del PIN de captura en dos flujos idénticos, uno para la captura y otro para la vista previa. En el siguiente diagrama se muestra este proceso.

![gráfico de captura con filtro Smart Tee](images/vidcap05.png)

El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente el filtro de forma inteligente si es necesario. Sin embargo, si usa métodos de **IGraphBuilder** para compilar el gráfico, y no **RenderStream**, puede que tenga que insertar el filtro de tee inteligente.

Antes de representar PIN en el filtro de captura, compruebe si el filtro tiene un PIN de vista previa o un PIN de puerto de vídeo. En caso contrario, y desea obtener una vista previa, agregue el filtro Smart Tee al gráfico y conéctelo al pin de captura en el filtro de captura.

> [!Note]  
> Puede tratar un PIN de puerto de vídeo (VP) como un tipo de PIN de vista previa, por lo que un filtro con el código de VP no necesita un filtro Smart tee. Sin embargo, los VP PIN tienen otros requisitos especiales. Para obtener más información, consulte [pines del puerto de vídeo](video-port-pins.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Combinación de captura de vídeo y vista previa](combining-video-capture-and-preview.md)
</dt> <dt>

[Trabajar con categorías de PIN](working-with-pin-categories.md)
</dt> </dl>

 

 



