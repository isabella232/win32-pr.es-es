---
description: En Windows GDI+, un color es un valor de 32 bits con 8 bits cada uno para alfa, rojo, verde y azul.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Líneas y rellenos con mezcla alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64096bbabc632ad7c2b159191ad21b3b09f3801a486f27679118008e4927e88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977805"
---
# <a name="alpha-blending-lines-and-fills"></a>Líneas y rellenos con mezcla alfa

En Windows GDI+, un color es un valor de 32 bits con 8 bits cada uno para alfa, rojo, verde y azul. El valor alfa indica la transparencia del color, la medida en que el color se combina con el color de fondo. Los valores alfa oscilan entre 0 y 255, donde 0 representa un color totalmente transparente y 255 representa un color totalmente opaco.

La combinación alfa es una combinación píxel a píxel de datos de color de origen y de fondo. Cada uno de los tres componentes (rojo, verde y azul) de un color de origen determinado se combina con el componente correspondiente del color de fondo según la fórmula siguiente:

displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255

Por ejemplo, suponga que el componente rojo del color de origen es 150 y el componente rojo del color de fondo es 100. Si el valor alfa es 200, el componente rojo del color resultante se calcula de la siguiente manera:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

En los temas siguientes se trata la combinación alfa con más detalle:

-   [Dibujo de líneas opacas y semitransparentes](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Dibujo con pinceles opacos y semitransparentes](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Usar el modo de composición para controlar la combinación alfa](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Uso una matriz de colores para establecer valores alfa en imágenes](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Establecer los valores alfa de píxeles individuales](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



