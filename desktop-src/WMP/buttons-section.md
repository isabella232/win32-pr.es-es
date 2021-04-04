---
title: Sección botones
description: Sección botones
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Aspectos de Windows Media Player Mobile, sección de botones
- aspectos, sección de botones
- crear máscaras, sección de botones
- escribir código para máscaras, sección de botones
- botones en máscaras, sección botones
- archivos de definición de máscara, sección de botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075942"
---
# <a name="buttons-section"></a>Sección botones

A continuación, debe definir los botones que se van a usar:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



En esta sección se definen cuatro botones. La página que está viendo puede ajustar estas líneas, pero cuando escribe en el código, no debe ajustar las líneas; es decir, cada línea debe estar completa y terminar con una marca de párrafo.

> [!Note]  
> Los tipos de botones están desusados en las máscaras de Windows Media Player 10 Mobile o posterior. En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.

 

Para cada botón debe definir la función, el tipo, la ubicación, el origen de la imagen insertada, el origen deshabilitado y el color (para los botones de tipo de acceso). Además, para el botón PlayPause, debe definir los orígenes de imagen normales e insertados para el estado de pausa.

Para obtener más información sobre la sección de botones del archivo de definición de máscara, vea [botones](buttons.md) en la referencia de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




