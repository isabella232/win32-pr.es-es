---
description: Elección del representador de vídeo correcto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Elección del representador de vídeo correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677193"
---
# <a name="choosing-the-right-video-renderer"></a>Elección del representador de vídeo correcto

DirectShow proporciona varios filtros de representador de vídeo, resumidos en la tabla siguiente.



| Filter                                                                  | Observaciones                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) | Usa Direct3D 9. Requiere Windows Vista o posterior. |
| [Procesador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Usa Direct3D 9. Requiere Windows XP o posterior.    |
| [Filtro de combinación de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Utiliza DirectDraw. Requiere Windows XP o posterior.    |
| [Mezclador de superposición](using-the-overlay-mixer-in-video-capture.md)           | Admite superposiciones de hardware a través de DirectDraw.    |
| Filtro de [representador de vídeo](video-renderer-filter.md) heredado.              | Utiliza DirectDraw o (rara vez) GDI                   |



 

El representador que se va a usar depende en gran medida de las versiones de Windows que necesite admitir.

-   En Windows Vista y versiones posteriores, las aplicaciones deben usar EVR si el hardware lo admite. De lo contrario, revertir a VMR-9 o VMR-7. EVR ofrece un mejor rendimiento y una mejor calidad de vídeo que los representadores anteriores. Además, está diseñado para funcionar con el Administrador de ventanas de escritorio (DWM).
-   Antes de Windows Vista, use VMR-9 Si el hardware lo admite y la funcionalidad de puerto de vídeo no es necesaria. De lo contrario, use VMR-7.
-   En sistemas más antiguos, es posible que tenga que usar el mezclador de superposición (para la compatibilidad con el puerto de vídeo o la superposición de hardware) o el filtro de representador de vídeo heredado.

Los métodos [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) y [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usan de forma predeterminada VMR-7. Si el hardware no admite la versión VMR-7, estos métodos se revierten al filtro de representador de vídeo heredado. EVR y VMR-9 nunca son los representadores predeterminados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



