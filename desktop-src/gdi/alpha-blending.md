---
description: La combinación alfa se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Combinación alfa (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb59f6b628236124305e4564803fa826c279bfdc2353725a62029b293cb1e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470135"
---
# <a name="alpha-blending-windows-gdi"></a>Combinación alfa (Windows GDI)

*La combinación alfa* se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes. Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como *su canal alfa*. El canal alfa normalmente contiene tantos bits como un canal de color. Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, de 0 (todo el mapa de bits es transparente) a 255 (todo el mapa de bits es opaco).

Los mecanismos de combinación alfa se invocan mediante una llamada [**a AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), que hace referencia a la [**estructura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)

Los valores alfa por píxel solo se admiten para RGB bi de 32 \_ bpp. Esta fórmula se define como:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Esto se representa en memoria, como se muestra en la tabla siguiente.

:::row:::
    :::column:::
        31:24
    :::column-end:::
    :::column:::
        23:16
    :::column-end:::
    :::column:::
        15:08
    :::column-end:::
    :::column:::
        07:00
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        Alpha
    :::column-end:::
    :::column:::
        Rojo
    :::column-end:::
    :::column:::
        Verde
    :::column-end:::
    :::column:::
        Azul
    :::column-end:::
:::row-end:::

Los mapas de bits también se pueden mostrar con un factor de transparencia aplicado a todo el mapa de bits. Cualquier formato de mapa de bits se puede mostrar con un valor alfa constante global estableciendo **SourceConstantAlpha** en la [**estructura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) El valor alfa constante global tiene 256 niveles de transparencia, de 0 (todo el mapa de bits es completamente transparente) a 255 (todo el mapa de bits es completamente opaco). El valor alfa constante global se combina con el valor alfa por píxel.

Para obtener un ejemplo, vea [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).

 

 



