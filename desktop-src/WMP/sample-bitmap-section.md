---
title: Sección de mapa de bits de ejemplo
description: Sección de mapa de bits de ejemplo
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- referencia para máscaras, mapas de bits
- mapas de bits en máscaras, sección de mapas de bits
- archivos de definición de máscara, sección de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903686"
---
# <a name="sample-bitmap-section"></a>Sección de mapa de bits de ejemplo

Las siguientes líneas muestran una sección típica de mapas de bits de un archivo de definición de máscara:


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



Esto define cinco mapas de bits que se usan para crear una imagen de fondo, imágenes para botones deshabilitados y insertados, una imagen de región para botones de región y una superimagen para trackbars.

> [!Note]  
> Los mapas de bits de región y súper están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mapas de bits**](bitmaps.md)
</dt> </dl>

 

 




