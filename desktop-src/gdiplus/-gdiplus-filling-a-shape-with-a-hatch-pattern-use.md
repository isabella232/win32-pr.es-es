---
description: 'Un patrón de trama se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón en el fondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Relleno de una forma con un patrón de trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988130"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Relleno de una forma con un patrón de trama

Un patrón de trama se realiza a partir de dos colores: uno para el fondo y otro para las líneas que forman el patrón en el fondo. Para rellenar una forma cerrada con un patrón de trama, use un objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) . En el ejemplo siguiente se muestra cómo rellenar una elipse con un patrón de trama:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



En la ilustración siguiente se muestra la elipse rellenada.

![Ilustración de una elipse rellena con el patrón de trama de las líneas horizontales sobre un fondo sólido](images/hatch1.png)

El constructor [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) toma tres argumentos: el estilo de trama, el color de la línea de sombreado y el color del fondo. El argumento de estilo de trama puede ser cualquier elemento de la enumeración [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) . Hay más de 50 elementos en la enumeración **HatchStyle** ; algunos de esos elementos se muestran en la lista siguiente:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



