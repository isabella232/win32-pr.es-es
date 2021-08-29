---
title: Sección Botones
description: Sección Botones
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Reproductor de Windows Media Máscaras móviles, sección Botones
- máscaras, sección Botones
- crear máscaras, sección Botones
- escribir código para máscaras, sección Botones
- botones en máscaras, sección Botones
- archivos de definición de máscara, sección Botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c64c055ee5ef4bc758838b531cf9052548f8673e18219970b750eb092d57fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997744"
---
# <a name="buttons-section"></a>Sección Botones

A continuación, debe definir los botones que va a usar:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



Hay cuatro botones definidos en esta sección. La página que está viendo puede encapsular estas líneas, pero cuando escribe en el código, no debe ajustar las líneas; es decir, cada línea debe estar completa y terminar con una marca de párrafo.

> [!Note]  
> Los tipos de botones están en desuso Reproductor de Windows Media 10 máscaras móviles o posteriores. En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.

 

Para cada botón debe definir la función, el tipo, la ubicación, el origen de la imagen inserda, el origen deshabilitado y el color (para los botones de tipo de llamada). Además, para el botón PlayPause , debe definir los orígenes de imágenes normales e insertadas para el estado en pausa.

Para obtener más información sobre la sección Botones del archivo de definición de máscara, vea [Botones en](buttons.md) la referencia de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




