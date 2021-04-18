---
description: La combinación alfa se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Combinación alfa (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985074"
---
# <a name="alpha-blending-windows-gdi"></a>Combinación alfa (Windows GDI)

La *combinación alfa* se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes. Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como *canal alfa*. Normalmente, el canal alfa contiene tantos bits como un canal de color. Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, desde 0 (el mapa de bits completo es transparente) hasta 255 (todo el mapa de bits es opaco).

Los mecanismos de combinación alfa se invocan llamando a [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), que hace referencia a la estructura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .

Los valores alfa por píxel solo se admiten para 32-bpp BI \_ RGB. Esta fórmula se define como:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Esto se representa en la memoria tal y como se muestra en la tabla siguiente.



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alpha | Rojo   | Verde | Azul  |



 

También es posible que se muestren los mapas de bits con un factor de transparencia aplicado a todo el mapa de bits. Cualquier formato de mapa de bits se puede mostrar con un valor alfa constante global estableciendo **SourceConstantAlpha** en la estructura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) . El valor alfa constante global tiene 256 niveles de transparencia, desde 0 (todo el mapa de bits es completamente transparente) hasta 255 (el mapa de bits completo es totalmente opaco). El valor alfa de constante global se combina con el valor alfa por píxel.

Para obtener un ejemplo, vea [alpha blending a Bitmap](alpha-blending-a-bitmap.md).

 

 



