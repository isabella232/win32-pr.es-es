---
description: Elección del representador de vídeo correcto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Elección del representador de vídeo correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b09c47357a61680902e47df080ae971b1d4bba4e569660aa3ad41df1c300c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131235"
---
# <a name="choosing-the-right-video-renderer"></a>Elección del representador de vídeo correcto

DirectShow proporciona varios filtros de representador de vídeo, resumidos en la tabla siguiente.



| Filter                                                                  | Comentarios                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) | Usa Direct3D 9. Requiere Windows Vista o posterior. |
| [Representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Usa Direct3D 9. Requiere Windows XP o posterior.    |
| [Filtro de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Usa DirectDraw. Requiere Windows XP o posterior.    |
| [Superposición Mixer](using-the-overlay-mixer-in-video-capture.md)           | Admite superposiciones de hardware a través de DirectDraw.    |
| Filtro [representador de vídeo](video-renderer-filter.md) heredado.              | Usa DirectDraw o (rara vez) GDI                   |



 

El representador que se va a usar depende en gran medida de las versiones Windows que necesita admitir.

-   En Windows Vista y versiones posteriores, las aplicaciones deben usar la EVR si el hardware lo admite. De lo contrario, vuelva a VMR-9 o VMR-7. El EVR ofrece un mejor rendimiento y una mejor calidad de vídeo que los representadores anteriores. Además, está diseñado para trabajar con el Administrador de ventanas de escritorio (DWM).
-   Antes de Windows Vista, use VMR-9 si el hardware lo admite y no se requiere la funcionalidad de puerto de vídeo. De lo contrario, use VMR-7.
-   En sistemas anteriores, es posible que deba usar el filtro Overlay Mixer (para la compatibilidad con el puerto de vídeo o la superposición de hardware) o el filtro De representador de vídeo heredado.

Los [**métodos IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) y [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usan VMR-7 de forma predeterminada. Si el hardware no es compatible con VMR-7, estos métodos retrocedemos al filtro representador de vídeo heredado. EVR y VMR-9 nunca son los representadores predeterminados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



