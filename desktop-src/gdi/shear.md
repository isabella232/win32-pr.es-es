---
description: Algunas aplicaciones proporcionan características que distorsionan objetos dibujados en el área de cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Sesgo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277853"
---
# <a name="shear"></a><span data-ttu-id="ddd4c-103">Sesgo</span><span class="sxs-lookup"><span data-stu-id="ddd4c-103">Shear</span></span>

<span data-ttu-id="ddd4c-104">Algunas aplicaciones proporcionan características que distorsionan objetos dibujados en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="ddd4c-105">Las aplicaciones que usan funciones de recorte usan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio global en el espacio de página.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="ddd4c-106">Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="ddd4c-107">Los miembros eM12 y eM21 de XFORM especifican las constantes de proporcionalidad horizontal y vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="ddd4c-108">Hay dos componentes de la *transformación de recorte*.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="ddd4c-109">El primero modifica las líneas verticales de un objeto; la segunda modifica las líneas horizontales.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="ddd4c-110">En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades distorsionado horizontalmente cuando se copia desde el espacio universal al espacio de la página.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![Ilustración en la que se muestra un rectángulo en el espacio del mundo y un trapeziod en el espacio de la página](images/cstrn-13.png)

<span data-ttu-id="ddd4c-112">Un recorte horizontal se puede representar mediante el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="ddd4c-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="ddd4c-113">donde x es la coordenada x original, SX es la constante de proporcionalidad y x ' es el resultado de la transformación de recorte.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="ddd4c-114">Un recorte vertical se puede representar mediante el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="ddd4c-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="ddd4c-115">donde y es la coordenada y original, SY es la constante de proporcionalidad e y ' es el resultado de la transformación de recorte.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="ddd4c-116">Las transformaciones de recorte horizontal y de recorte vertical se pueden combinar en una sola operación mediante una matriz de 2 por 2.</span><span class="sxs-lookup"><span data-stu-id="ddd4c-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="ddd4c-117">La matriz de 2 por 2 que generó la cizalla contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ddd4c-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



