---
title: Elección entre el modo RGBA y el Color-Index
description: En general, use el modo RGBA para las aplicaciones de OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como el sombreado, la iluminación, la asignación de colores, la niebla, el suavizado de contorno y la fusión.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL en Windows, modo RGBA
- OpenGL en Windows, modo de índice de color
- Modo RGBA de OpenGL
- modo de índice de color OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775960"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Elección entre el modo RGBA y el Color-Index

En general, use el modo RGBA para las aplicaciones de OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como el sombreado, la iluminación, la asignación de colores, la niebla, el suavizado de contorno y la fusión.

Considere la posibilidad de usar el modo de índice de color en los casos siguientes:

-   Si tiene un número limitado de bitplanes disponibles; el modo de índice de color puede producir un sombreado menos grueso que el modo RGBA.
-   Si no le preocupa el uso de colores "reales"; por ejemplo, el uso de varios colores en un mapa topográfico para designar elevaciones relativas.
-   Al migrar una aplicación existente que utiliza el modo de índice de color en gran medida.
-   Cuando desee usar la animación y los efectos de mapa de colores en la aplicación. (Esto no es posible en dispositivos de color verdadero).

 

 




