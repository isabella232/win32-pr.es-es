---
description: VMR frente a
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: Los representadores de DirectShow anteriores y VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666769"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>Los representadores de DirectShow anteriores y VMR

Con los filtros antiguos, se necesitarán representadores diferentes en el gráfico en función de la configuración de hardware.

El filtro de [representador de vídeo](video-renderer-filter.md) se ha utilizado para representar un único flujo de vídeo en escenarios de puertos que no son de vídeo. Se basó en tecnología de hardware de gráficos que ahora es superior a cinco años y en una versión anterior de DirectDraw. En ciertos escenarios, usa GDI para la representación. Esto se hace para conservar los recursos de vídeo, que eran mucho más limitados hace cinco años, o bien para superar las limitaciones de DirectDraw relacionadas con la compatibilidad con varios monitores. Ni VMR-7 ni VMR-9 usan GDI para la representación; VMR-7 se basa completamente en DirectDraw 7 y VMR-9 se basa en Direct3D 9.

En escenarios que implican un puerto de vídeo o varios flujos de entrada de vídeo, antes de la VMR, el filtro de [mezclador de superposición](overlay-mixer-filter.md) se usaba para la representación. Este filtro solo usa la superposición de hardware de la tarjeta gráfica y, por lo general, está limitado a la superficie de una superposición proporcionada por la mayoría de las tarjetas. El mezclador de superposición realiza la incrustación de color de destino, pero no es capaz de la combinación alfa. Dado que no tiene un administrador de ventanas, debe usar un segundo filtro, el representador de vídeo, para la administración de ventanas. La VMR es capaz de ofrecer una combinación alfa verdadera y puede crear varias superposiciones en el software además de las superposiciones de hardware.

En los escenarios de puerto de vídeo en los que las aplicaciones superponen subtítulos (CC) u otros datos de VBI en el vídeo, se necesitaba un filtro adicional, el [asignador de superficie de VBI](vbi-surface-allocator.md), para asignar la memoria de vídeo adicional para el texto de VBI. En el caso de los ISV, VMR-7 simplifica el desarrollo de aplicaciones mediante la combinación de la funcionalidad de asignación y representación en un único filtro que se utiliza en todos los escenarios. Con la VMR, el asignador de superficie de VBI ya no es necesario. Este filtro se reemplaza en Windows XP por el nuevo filtro del [Administrador de puertos de vídeo](video-port-manager.md) que realiza todas las tareas de puerto de vídeo realizadas previamente por el mezclador de superposición.

> [!Note]  
> VMR-9 no admite puertos de vídeo.

 

La VMR es más sólida que los representadores anteriores, en parte porque solo usa DirectDraw 7 (o Direct3D 9 Si usa las interfaces VMR-9), en contraposición a los representadores antiguos que usaban una combinación de interfaces de versiones anteriores y más recientes de DirectDraw. La VMR también emplea un nuevo mecanismo de presentación de imágenes diseñado para generaciones actuales y futuras de adaptadores, que tienen compatibilidad con Direct3D, mayor ancho de banda de memoria de vídeo y VRAM y características de aceleración de hardware. Con la VMR, el enfoque es el procesamiento de front-end y la dependencia reducida de los puertos de vídeo y las superposiciones. Pero incluso con toda su nueva funcionalidad, VMR está diseñado para ofrecer compatibilidad máxima con las aplicaciones existentes.

La VMR también es extensible. Las aplicaciones pueden proporcionar sus propios subcomponentes para realizar efectos de vídeo personalizados o tomar el control de la asignación y el proceso de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la presentación de la combinación de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



