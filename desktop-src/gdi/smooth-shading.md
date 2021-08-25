---
description: El sombreado suave es un método de sombreado de una región con un degradado de color.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Sombreado suave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5bfa54fef8d0a6810a3230e88e4e3144f7ecf4b62f7313f5daf4213e948c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965205"
---
# <a name="smooth-shading"></a>Sombreado suave

*El sombreado suave es* un método de sombreado de una región con un degradado de color. La inclusión de información de color, junto con los límites de la primitiva de dibujo, especifica el degradado de color. GDI interpola linealmente el color del interior de la primitiva pasada en los puntos de conexión de color. La información de color y vértice se incluye con información de posición en la [**estructura TRIVERTEX.**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)

Use la [**función GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para rellenar una estructura de triángulo o rectángulo. Para rellenar un triángulo con sombreado suave, llame a **GradientFill** con los tres puntos de conexión del triángulo. Para rellenar un rectángulo con sombreado suave, llame a **GradientFill** con las coordenadas del rectángulo superior izquierdo e inferior derecho. **GradientFill hace** referencia a [**las estructuras TRIVERTEX,**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) [**GRADIENT \_ RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)y [**GRADIENT \_ TRIANGLE.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)

Para obtener un ejemplo, vea [Dibujar un triángulo sombreado.](drawing-a-shaded-triangle.md)

 

 



