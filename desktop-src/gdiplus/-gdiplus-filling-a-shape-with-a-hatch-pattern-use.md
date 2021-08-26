---
description: 'Un patrón de sombreado se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón sobre el fondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Rellenar una forma con un patrón de sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b571ab09dc91c037e0cc89a2b107c2f8d253b832b593bb32a169bc970295d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015105"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Rellenar una forma con un patrón de sombreado

Un patrón de sombreado se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón sobre el fondo. Para rellenar una forma cerrada con un patrón de sombreado, use un [**objeto HatchBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) En el ejemplo siguiente se muestra cómo rellenar una elipse con un patrón de sombreado:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



En la ilustración siguiente se muestra la elipse rellena.

![ilustración de una elipse rellena con el patrón de sombreado de líneas horizontales sobre un fondo sólido](images/hatch1.png)

El constructor [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) toma tres argumentos: el estilo de sombreado, el color de la línea de sombreado y el color del fondo. El argumento de estilo de sombreado puede ser cualquier elemento de la [**enumeración HatchStyle.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) Hay más de cincuenta elementos en la **enumeración HatchStyle;** Algunos de esos elementos se muestran en la lista siguiente:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



