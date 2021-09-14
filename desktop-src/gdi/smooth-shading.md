---
description: El sombreado suave es un método para sombrear una región con un degradado de color.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Sombreado suave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072446"
---
# <a name="smooth-shading"></a>Sombreado suave

*El sombreado suave es* un método para sombrear una región con un degradado de color. La inclusión de información de color, junto con los límites del dibujo primitivo, especifica el degradado de color. GDI interpola linealmente el color del interior de la primitiva pasada en los puntos de conexión de color. La información de color y vértice se incluye con información de posición en la [**estructura TRIVERTEX.**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)

Use la [**función GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para rellenar una estructura de triángulo o rectángulo. Para rellenar un triángulo con sombreado suave, llame **a GradientFill** con los tres puntos de conexión del triángulo. Para rellenar un rectángulo con sombreado suave, llame a **GradientFill** con las coordenadas del rectángulo superior izquierdo e inferior derecho. **GradientFill hace** referencia a [**las estructuras TRIVERTEX,**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) [**GRADIENT \_ RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)y [**GRADIENT \_ TRIANGLE.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)

Para obtener un ejemplo, vea [Dibujar un triángulo sombreado.](drawing-a-shaded-triangle.md)

 

 



