---
description: El sombreado suave es un método para sombrear una región con un degradado de color.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Sombreado suave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277852"
---
# <a name="smooth-shading"></a>Sombreado suave

El *sombreado suave* es un método para sombrear una región con un degradado de color. Al incluir la información de color, junto con los límites del dibujo primitivo, se especifica el degradado de color. GDI interpola linealmente el color del interior de la primitiva pasada en los extremos de color. La información de color y de vértices se incluye con la información de posición en la estructura de [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .

Utilice la función [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para rellenar una estructura de triángulo o rectángulo. Para rellenar un triángulo con un sombreado suave, llame a **GradientFill** con los tres puntos de conexión de triángulo. Para rellenar un rectángulo con un sombreado suave, llame a **GradientFill** con las coordenadas superior izquierda e inferior derecha del rectángulo. **GradientFill** hace referencia a las estructuras de [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ rectángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)y [**\_ triángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .

Para obtener un ejemplo, vea [dibujar un triángulo sombreado](drawing-a-shaded-triangle.md).

 

 



