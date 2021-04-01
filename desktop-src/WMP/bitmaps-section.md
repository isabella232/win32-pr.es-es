---
title: Sección de mapas de bits
description: Sección de mapas de bits
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- crear máscaras, sección de mapas de bits
- escribir código para máscaras, sección de mapas de bits
- mapas de bits en máscaras, sección de mapas de bits
- archivos de definición de máscara, sección de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075639"
---
# <a name="bitmaps-section"></a>Sección de mapas de bits

A continuación, debe tener una sección que defina cada uno de los archivos de mapa de bits. Cada tipo de mapa de bits que usará debe tener un archivo asignado, aunque puede tener más de un tipo con el mismo mapa de bits.


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



La sección de mapas de bits debe comenzar con los mapas de bits de Word entre corchetes y, a continuación, una línea para cada tipo de mapa de bits que desee definir. En este ejemplo, se definieron cinco tipos de mapas de bits. Para obtener más información sobre la sección de mapas de bits, vea [mapas de bits](bitmaps.md) en la referencia de máscara.

> [!Note]  
> Los mapas de bits de región y súper están desusados en las máscaras de Windows Media Player 10 Mobile o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




