---
description: La mayoría de las aplicaciones de CAD y de dibujo proporcionan características que escalan la salida creada por el usuario.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Ampliación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985811"
---
# <a name="scaling"></a><span data-ttu-id="a7b7c-103">Ampliación</span><span class="sxs-lookup"><span data-stu-id="a7b7c-103">Scaling</span></span>

<span data-ttu-id="a7b7c-104">La mayoría de las aplicaciones de CAD y de dibujo proporcionan características que escalan la salida creada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="a7b7c-105">Las aplicaciones que incluyen funcionalidades de escalado (o zoom) llaman a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio universal adecuado en el espacio de la página.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="a7b7c-106">Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="a7b7c-107">Los miembros eM11 y eM22 de XFORM especifican los componentes de escalado horizontal y vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="a7b7c-108">Cuando se produce el *escalado* , las líneas verticales y horizontales (o vectores) que constituyen un objeto se ajustan o se comprimen con respecto al eje x o y.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="a7b7c-109">En la ilustración siguiente se muestra un rectángulo de una unidad de 20 por 20 escalada verticalmente al doble de su altura original cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![Ilustración en la que se muestra un pequeño rectángulo en el espacio del mundo y otro más alto en el espacio de la página](images/cstrn-10.png)

<span data-ttu-id="a7b7c-111">En la ilustración anterior, las líneas verticales que definen la medida lateral del rectángulo original 20 unidades, mientras que las líneas verticales que definen los lados del rectángulo escalado miden 40 unidades.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="a7b7c-112">El escalado vertical puede representarse mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="a7b7c-113">Donde y ' es la nueva longitud, y es la longitud original y DY es el factor de escala vertical.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="a7b7c-114">El escalado horizontal se puede representar mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="a7b7c-115">Donde x es la nueva longitud, x es la longitud original y DX es el factor de escala horizontal.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="a7b7c-116">Las transformaciones de escalado vertical y horizontal se pueden combinar en una sola operación mediante una matriz de 2 por 2.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="a7b7c-117">La matriz de 2 por 2 que generó la transformación de escala contiene los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="a7b7c-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



