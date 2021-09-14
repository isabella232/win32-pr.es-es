---
description: Usar el representador de mezcla de vídeo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Usar el representador de mezcla de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275028"
---
# <a name="using-the-video-mixing-renderer"></a>Usar el representador de mezcla de vídeo

En cuanto al rendimiento y la amplitud de las características, el filtro Representador de mezcla de vídeo (VMR) representa la próxima generación en la representación de vídeo en la plataforma Windows vídeo. VmR reemplaza a overlay [Mixer](overlay-mixer-filter.md) [Video Renderer](video-renderer-filter.md)y agrega muchas características de combinación nuevas.

Hay dos versiones de VMR:

-   VMR-7, que usa DirectDraw 7 para la representación.
-   VMR-9, que usa Direct3D 9.

VMR-7 está disponible en Windows XP y versiones posteriores, pero no está disponible para redistribución. VMR-9 está disponible para su redistribución en todas las plataformas compatibles con DirectX 9. Los dos filtros de VMR son muy similares en su implementación y en las interfaces que exponen.

VMR-9 tiene su propio CLSID y su propio conjunto de interfaces, estructuras y tipos de enumeración que no siempre son idénticos a los tipos de datos correspondientes para VMR-7, debido a las diferencias subyacentes entre DirectDraw 7 y Direct3D 9. Todas las interfaces VMR-9 terminan con "9", por ejemplo **IVMRStreamConfig9,** y las estructuras y los tipos de enumeración tienen "VMR9" en su nombre para distinguirlos de los tipos de datos usados con VMR-7.

Para garantizar la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema. Para usar VMR-9, debe agregarlo explícitamente al gráfico de filtros mediante el método [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) y configurarlo antes de conectarlo a cualquier filtro ascendente.

Este artículo contiene las secciones siguientes. Excepto donde se indica, la información de estas secciones se aplica a los filtros VMR-7 y VMR-9.

-   [Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
-   [Modos de funcionamiento de VMR](vmr-modes-of-operation.md)
-   [Creación de un filtro VMR-9 Graph](building-a-vmr-9-filter-graph.md)
-   [Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
-   [Establecer preferencias de desinterlace](setting-deinterlace-preferences.md)
-   [Uso de VMR para DirectShow desarrolladores de filtros](using-the-vmr-for-directshow-filter-developers.md)
-   [Uso del Protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



