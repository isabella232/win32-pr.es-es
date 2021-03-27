---
description: Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Rellenar formas con un pincel de degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997493"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Rellenar formas con un pincel de degradado

Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente. Por ejemplo, puede usar un degradado horizontal para rellenar una forma con un color que cambie gradualmente a medida que se desplaza desde el borde izquierdo de la forma hasta el borde derecho. Imagine un rectángulo con un borde izquierdo que sea negro (representado por los componentes rojo, verde y azul 0, 0, 0) y un borde derecho rojo (representado por 255, 0,0). Si el rectángulo tiene una anchura de 256 píxeles, el componente rojo de un píxel determinado será uno mayor que el componente rojo del píxel situado a su izquierda. El píxel situado más a la izquierda de una fila tiene componentes de color (0,0), el segundo píxel (1, 0, 0), el tercer píxel tiene (2, 0, 0), y así sucesivamente, hasta que llegue al píxel más a la derecha, que tiene componentes de color (255, 0,0). Estos valores de color interpolados constituyen el degradado de color.

Un degradado lineal cambia el color a medida que se mueve horizontalmente, verticalmente o en paralelo a una línea inclinada especificada. Un degradado de trazado cambia el color a medida que se mueve sobre el interior y el límite de un trazado. Puede personalizar los degradados de trazado para lograr una gran variedad de efectos.

GDI+ proporciona las clases [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) y [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , que heredan de la clase [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

En los temas siguientes se tratan los degradados lineales y de trazado con más detalle:

-   [Crear un degradado lineal](-gdiplus-creating-a-linear-gradient-use.md)
-   [Crear un degradado de trazado](-gdiplus-creating-a-path-gradient-use.md)
-   [Aplicar la corrección gamma a un degradado](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



