---
title: Sección Mapas de bits
description: Sección Mapas de bits
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Reproductor de Windows Media Máscaras móviles, mapas de bits
- máscaras, mapas de bits
- crear máscaras, sección Mapas de bits
- escribir código para máscaras, sección Mapas de bits
- mapas de bits en máscaras, sección Mapas de bits
- archivos de definición de máscara, sección Mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889556"
---
# <a name="bitmaps-section"></a>Sección Mapas de bits

A continuación, debe tener una sección que defina cada uno de los archivos de mapa de bits. Cada tipo de mapa de bits que usará debe tener asignado un archivo, aunque puede tener más de un tipo con el mismo mapa de bits.


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



La sección Mapas de bits debe comenzar con la palabra Mapas de bits entre corchetes y, a continuación, una línea para cada tipo de mapa de bits que quiera definir. En este ejemplo, se definieron cinco tipos de mapas de bits. Para obtener más información sobre la sección Mapas de bits, vea [Mapas de bits](bitmaps.md) en la referencia de máscara.

> [!Note]  
> Los mapas de bits Región y Super están en desuso Reproductor de Windows Media 10 máscaras móviles o posteriores.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




