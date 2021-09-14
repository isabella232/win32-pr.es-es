---
title: Sección de mapa de bits de ejemplo
description: Sección de mapa de bits de ejemplo
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Reproductor de Windows Media Máscaras móviles, mapas de bits
- máscaras, mapas de bits
- referencia de máscaras, mapas de bits
- mapas de bits en máscaras, sección Mapas de bits
- archivos de definición de máscara, sección Mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070877"
---
# <a name="sample-bitmap-section"></a>Sección de mapa de bits de ejemplo

Las líneas siguientes muestran una sección de mapas de bits típica de un archivo de definición de máscara:


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



Esto define cinco mapas de bits que se usan para crear una imagen de fondo, imágenes para botones deshabilitados e presionados, una imagen de región para los botones de región y una imagen super para barras de seguimiento.

> [!Note]  
> Los mapas de bits Region y Super están en desuso en máscaras para Reproductor de Windows Media 10 Mobile o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mapas de bits**](bitmaps.md)
</dt> </dl>

 

 




