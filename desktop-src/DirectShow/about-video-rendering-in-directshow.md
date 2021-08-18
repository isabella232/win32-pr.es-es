---
description: Acerca de la representación de vídeo en DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Acerca de la representación de vídeo en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d2d39cab75f2943a052b157296673f504a1220c17369d5a1639215f074a359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873675"
---
# <a name="about-video-rendering-in-directshow"></a>Acerca de la representación de vídeo en DirectShow

DirectShow proporciona varios filtros que representan vídeo:

-   [Filtro de representador de](video-renderer-filter.md) vídeo. Este filtro está disponible para todas las plataformas que admiten DirectX y no tiene requisitos del sistema concretos. El representador de vídeo usa DirectDraw siempre que sea posible para representar el vídeo; de lo contrario, usa GDI. Este filtro es el representador de vídeo predeterminado en plataformas anteriores a Windows XP.
-   [Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 está disponible en Windows XP, donde es el representador de vídeo predeterminado. VMR-7 siempre usa DirectDraw 7 para la representación. Proporciona muchas características eficaces que no están disponibles en el filtro de representador de vídeo anterior, incluido un modelo de complemento donde la aplicación controla las superficies de DirectDraw usadas para la representación.
-   [Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 es una versión más reciente del representador de mezcla de vídeo que usa Direct3D 9 para la representación. Está disponible para todas las plataformas que admiten DirectX. Sin embargo, no es el representador predeterminado, ya que tiene requisitos del sistema más altos que el filtro Representador de vídeo.
-   El [filtro overlay Mixer](overlay-mixer-filter.md) está diseñado específicamente para la reproducción de DVD y la difusión de vídeo. También admite las extensiones de puerto de vídeo (VPN), lo que le permite trabajar con descodificadores MPEG-2 de hardware o de televisión análoga que envían vídeo directamente a la tarjeta gráfica.
-   El [**filtro Representador de vídeo**](enhanced-video-renderer-filter.md) mejorado (EVR) está disponible a partir de Windows Vista. Ofrece un rendimiento de vídeo mejorado en comparación con los representadores de vídeo anteriores, especialmente cuando Windows la composición de escritorio de Vista está habilitada.

Por lo general, el EVR es el preferido para las aplicaciones destinadas a Windows Vista o versiones posteriores, y vmr-9 es preferible para las aplicaciones que se ejecutan en versiones anteriores de Windows. Para obtener más información sobre el uso de los filtros VMR-7 y VMR-9, consulte Uso del representador [de mezcla de vídeo.](using-the-video-mixing-renderer.md)

Modo de ventana y modo sin ventanas

Un DirectShow de vídeo puede funcionar en modo *de* ventana o *en modo sin* ventana.

-   En modo de ventana, el representador crea su propia ventana para mostrar el vídeo. Normalmente, esta ventana se convierte en el elemento secundario de una ventana de aplicación. Para obtener más información, [vea Using Windowed Mode](using-windowed-mode.md).
-   En modo sin ventanas, el representador dibuja el vídeo directamente en una ventana de aplicación. No crea su propia ventana. Para obtener más información sobre este modo, vea [Using Windowless Mode](using-windowless-mode.md).

El filtro Representador de vídeo solo admite el modo de ventana. Los filtros VMR-7 y VMR-9 admiten ambos modos. Tienen como valor predeterminado el modo de ventana por compatibilidad con versiones anteriores, pero se prefiere el modo sin ventanas. EvR solo admite el modo sin ventanas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



