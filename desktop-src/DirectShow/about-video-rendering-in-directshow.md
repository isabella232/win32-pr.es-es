---
description: Acerca de la representación de vídeo en DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Acerca de la representación de vídeo en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906831"
---
# <a name="about-video-rendering-in-directshow"></a>Acerca de la representación de vídeo en DirectShow

DirectShow proporciona varios filtros que representan vídeo:

-   Filtro de [representador de vídeo](video-renderer-filter.md) . Este filtro está disponible para todas las plataformas que admiten DirectX y no tiene requisitos de sistema concretos. El representador de vídeo usa DirectDraw siempre que sea posible para representar el vídeo; de lo contrario, usa GDI. Este filtro es el representador de vídeo predeterminado en plataformas anteriores a Windows XP.
-   [Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 está disponible en Windows XP, donde es el representador de vídeo predeterminado. VMR-7 siempre usa DirectDraw 7 para la representación. Proporciona muchas características eficaces que no están disponibles en el filtro de representador de vídeo más antiguo, incluido un modelo de complemento en el que la aplicación controla las superficies de DirectDraw usadas para la representación.
-   [Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 es una versión más reciente del representador de mezcla de vídeo que usa Direct3D 9 para la representación. Está disponible para todas las plataformas compatibles con DirectX. Sin embargo, no es el representador predeterminado porque tiene requisitos de sistema más altos que el filtro de representador de vídeo.
-   El filtro de [mezclador de superposición](overlay-mixer-filter.md) está diseñado específicamente para la reproducción de DVD y vídeo de difusión. También admite extensiones de puerto de vídeo (VPEs), lo que permite que funcione con descodificadores de hardware MPEG-2 o sintonizadores de TV analógicos que envían vídeo directamente a la tarjeta gráfica.
-   El filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) está disponible a partir de Windows Vista. Ofrece un rendimiento de vídeo mejorado en comparación con representadores de vídeo anteriores, especialmente cuando la composición de escritorio de Windows Vista está habilitada.

Por lo general, se prefiere el EVR para las aplicaciones que tienen como destino Windows Vista o posterior, y se prefiere VMR-9 para las aplicaciones que se ejecutan en versiones anteriores de Windows. Para obtener más información sobre el uso de los filtros VMR-7 y VMR-9, consulte [usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md).

Modo de ventana y modo sin ventanas

Un representador de vídeo de DirectShow puede funcionar en modo de *ventana* o en modo *sin ventanas* .

-   En el modo de ventana, el representador crea su propia ventana para mostrar el vídeo. Normalmente, esta ventana se convierte en el elemento secundario de una ventana de la aplicación. Para obtener más información, vea [usar el modo de ventana](using-windowed-mode.md).
-   En el modo sin ventanas, el representador dibuja el vídeo directamente en una ventana de la aplicación. No crea su propia ventana. Para obtener más información sobre este modo, consulte [usar el modo sin ventanas](using-windowless-mode.md).

El filtro de representador de vídeo solo admite el modo de ventana. Los filtros VMR-7 y VMR-9 admiten ambos modos. El modo predeterminado es el modo de ventana para la compatibilidad con versiones anteriores, pero se prefiere el modo sin ventanas. EVR admite únicamente el modo sin ventanas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



