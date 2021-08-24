---
description: VMR frente a
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR frente a representadores DirectShow anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9401361c5b258fdff09bf25351a79bf8315dabfb0c82636d7d8c3c9ffcdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903275"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR frente a representadores DirectShow anteriores

Con los filtros antiguos, se requieren representadores diferentes en el gráfico en función de la configuración de hardware.

El [filtro Representador de](video-renderer-filter.md) vídeo se usó para representar una sola secuencia de vídeo en escenarios de puerto que no son de vídeo. Se basaba en la tecnología de hardware gráfico que ahora tiene más de cinco años y en una versión anterior de DirectDraw. En determinados escenarios, usa GDI para la representación. Esto se hace para conservar los recursos de vídeo, que estaban mucho más limitados hace cinco años, o bien para superar las limitaciones de DirectDraw relacionadas con la compatibilidad con varios monitores. Ni VMR-7 ni VMR-9 usan GDI para la representación; VMR-7 se basa completamente en DirectDraw 7 y VMR-9 se basa en Direct3D 9.

En escenarios que implican un puerto de vídeo o varias secuencias de entrada de vídeo, antes de la VMR se usaba el filtro [overlay Mixer](overlay-mixer-filter.md) para la representación. Este filtro solo usa la superposición de hardware en la tarjeta gráfica, por lo que generalmente se limita a la superficie de superposición proporcionada por la mayoría de las tarjetas. El elemento Overlay Mixer la clave de color de destino, pero no es capaz de combinar alfa. Dado que no tiene un administrador de ventanas, debe usar un segundo filtro, el representador de vídeo, para la administración de ventanas. El VMR es capaz de realizar una mezcla alfa verdadera y puede crear varias superposiciones en el software además de las superposiciones de hardware.

En escenarios de puerto de vídeo en los que las aplicaciones superponeban subtítulos u otros datos de VBI en el vídeo, se requería un filtro adicional, el asignador de superficie de [VBI,](vbi-surface-allocator.md)para asignar la memoria de vídeo adicional para el texto de VBI. En el caso de los ISV, VMR-7 simplifica el desarrollo de aplicaciones mediante la combinación de la funcionalidad de asignación y representación en un único filtro que se usa en todos los escenarios. Con vmr, el asignador de superficie de VBI ya no es necesario. Este filtro se reemplaza en Windows XP por el nuevo filtro [Administrador](video-port-manager.md) de puertos de vídeo, que realiza todas las tareas de puerto de vídeo realizadas anteriormente por el administrador de superposición Mixer.

> [!Note]  
> VMR-9 no admite puertos de vídeo.

 

El VMR es más sólido que los representadores anteriores, en parte porque solo usa interfaces DirectDraw 7 (o Direct3D 9 si usa las interfaces VMR-9), en lugar de los representadores antiguos que usaban una combinación de interfaces de versiones anteriores y más recientes de DirectDraw. VmR también emplea un nuevo mecanismo de presentación de imágenes que está diseñado para las generaciones actuales y futuras de adaptadores, que admiten Direct3D, mayor ancho de banda de memoria de vídeo y VRAM, y características de aceleración de hardware. Con VMR, el foco se centra en el procesamiento de front-end y reduce la dependencia de los puertos de vídeo y las superposiciones. Pero incluso con todas sus nuevas funcionalidades, vmr está diseñado para ofrecer la máxima compatibilidad con las aplicaciones existentes.

El VMR también es extensible. Las aplicaciones pueden proporcionar sus propios componentes secundarios para realizar efectos de vídeo personalizados o tomar el control del proceso de asignación y representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



