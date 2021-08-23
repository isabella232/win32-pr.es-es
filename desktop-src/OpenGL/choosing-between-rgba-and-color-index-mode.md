---
title: Elegir entre RGBA y Color-Index automático
description: En general, use el modo RGBA para las aplicaciones OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como sombreado, iluminación, asignación de colores, paleta, suavizado de contorno y combinación.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL en Windows modo RGBA
- OpenGL en Windows, modo de índice de color
- OpenGL en modo RGBA
- color-index mode OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa78096369ec9ba01d6e0dcd3d67535a0d368ef7a5018d3679f9f64dcdf74d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554635"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Elegir entre RGBA y Color-Index automático

En general, use el modo RGBA para las aplicaciones OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como sombreado, iluminación, asignación de colores, paleta, suavizado de contorno y combinación.

Considere la posibilidad de usar el modo de índice de color en los casos siguientes:

-   Si tiene un número limitado de planos de bits disponibles; el modo de índice de color puede producir un sombreado menos general que el modo RGBA.
-   Si no le preocupa el uso de colores "reales"; por ejemplo, el uso de varios colores en un mapa topográfico para designar elevaciones relativas.
-   Al portear una aplicación existente que usa ampliamente el modo de índice de color.
-   Si desea usar la animación de mapa de colores y los efectos en la aplicación. (Esto no es posible en dispositivos de color verdadero).

 

 




