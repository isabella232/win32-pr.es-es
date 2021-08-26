---
description: Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Rellenar formas con un pincel de degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d471e9d3e2d7fb6d151d50ab3b5f10212874180b4554769b5c00a552085391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015055"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Rellenar formas con un pincel de degradado

Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente. Por ejemplo, puede usar un degradado horizontal para rellenar una forma con color que cambia gradualmente a medida que se mueve del borde izquierdo de la forma al borde derecho. Imagine un rectángulo con un borde izquierdo negro (representado por los componentes rojo, verde y azul 0, 0, 0) y un borde derecho rojo (representado por 255, 0, 0). Si el rectángulo tiene 256 píxeles de ancho, el componente rojo de un píxel determinado será uno mayor que el componente rojo del píxel a su izquierda. El píxel situado más a la izquierda de una fila tiene componentes de color (0, 0, 0), el segundo píxel tiene (1, 0, 0), el tercer píxel tiene (2, 0, 0), y así sucesivamente, hasta llegar al píxel más a la derecha, que tiene componentes de color (255, 0, 0). Estos valores de color interpolados son el degradado de color.

Un degradado lineal cambia de color a medida que se mueve horizontal, vertical o paralelamente a una línea inclinada especificada. Un degradado de trazado cambia de color a medida que se mueve por el interior y el límite de un trazado. Puede personalizar los degradados de trazado para lograr una amplia variedad de efectos.

GDI+ proporciona las [**clases LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) y [**PathGradientBrush,**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) que heredan de la [**clase Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

En los temas siguientes se tratan los degradados lineales y de trazado con más detalle:

-   [Crear un degradado lineal](-gdiplus-creating-a-linear-gradient-use.md)
-   [Crear un degradado de trazado](-gdiplus-creating-a-path-gradient-use.md)
-   [Aplicar corrección gamma a un degradado](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



