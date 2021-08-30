---
description: Uso del representador de mezcla de vídeo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Uso del representador de mezcla de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bbce539d21d756a7a1a648aab09105434da26ae586163f5f8bfe0edba77b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049505"
---
# <a name="using-the-video-mixing-renderer"></a>Uso del representador de mezcla de vídeo

En términos de rendimiento y amplitud de características, el filtro Representador de mezcla de vídeo (VMR) representa la próxima generación en la representación de vídeo en la plataforma Windows vídeo. VMR reemplaza a overlay [Mixer](overlay-mixer-filter.md) [Video Renderer](video-renderer-filter.md)y agrega muchas características de combinación nuevas.

Hay dos versiones de VMR:

-   VMR-7, que usa DirectDraw 7 para la representación.
-   VMR-9, que usa Direct3D 9.

VMR-7 está disponible en Windows XP y versiones posteriores, pero no está disponible para redistribución. VMR-9 está disponible para su redistribución en todas las plataformas compatibles con DirectX 9. Los dos filtros de VMR son muy similares en su implementación y en las interfaces que exponen.

VMR-9 tiene su propio CLSID y su propio conjunto de interfaces, estructuras y tipos de enumeración que no siempre son idénticos a los tipos de datos correspondientes para VMR-7, debido a las diferencias subyacentes entre DirectDraw 7 y Direct3D 9. Todas las interfaces VMR-9 terminan con "9", por **ejemplo, IVMRStreamConfig9,** y las estructuras y los tipos de enumeración tienen "VMR9" en su nombre para distinguirlos de los tipos de datos usados con VMR-7.

Para garantizar la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema. Para usar VMR-9, debe agregarlo explícitamente al gráfico de filtros mediante el método [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) y configurarlo antes de conectarlo a cualquier filtro ascendente.

Este artículo contiene las secciones siguientes. Excepto donde se indica, la información de estas secciones se aplica a los filtros VMR-7 y VMR-9.

-   [Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
-   [Modos de funcionamiento de VMR](vmr-modes-of-operation.md)
-   [Creación de un filtro VMR-9 Graph](building-a-vmr-9-filter-graph.md)
-   [Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
-   [Establecimiento de las preferencias de desinteresación](setting-deinterlace-preferences.md)
-   [Uso de VMR para DirectShow de filtros](using-the-vmr-for-directshow-filter-developers.md)
-   [Uso del protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



