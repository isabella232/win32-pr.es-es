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
# <a name="smooth-shading"></a><span data-ttu-id="ad10e-103">Sombreado suave</span><span class="sxs-lookup"><span data-stu-id="ad10e-103">Smooth Shading</span></span>

<span data-ttu-id="ad10e-104">El *sombreado suave* es un método para sombrear una región con un degradado de color.</span><span class="sxs-lookup"><span data-stu-id="ad10e-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="ad10e-105">Al incluir la información de color, junto con los límites del dibujo primitivo, se especifica el degradado de color.</span><span class="sxs-lookup"><span data-stu-id="ad10e-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="ad10e-106">GDI interpola linealmente el color del interior de la primitiva pasada en los extremos de color.</span><span class="sxs-lookup"><span data-stu-id="ad10e-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="ad10e-107">La información de color y de vértices se incluye con la información de posición en la estructura de [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .</span><span class="sxs-lookup"><span data-stu-id="ad10e-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="ad10e-108">Utilice la función [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para rellenar una estructura de triángulo o rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ad10e-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="ad10e-109">Para rellenar un triángulo con un sombreado suave, llame a **GradientFill** con los tres puntos de conexión de triángulo.</span><span class="sxs-lookup"><span data-stu-id="ad10e-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="ad10e-110">Para rellenar un rectángulo con un sombreado suave, llame a **GradientFill** con las coordenadas superior izquierda e inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ad10e-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="ad10e-111">**GradientFill** hace referencia a las estructuras de [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ rectángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)y [**\_ triángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .</span><span class="sxs-lookup"><span data-stu-id="ad10e-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="ad10e-112">Para obtener un ejemplo, vea [dibujar un triángulo sombreado](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="ad10e-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



