---
description: Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987703"
---
# <a name="translation"></a><span data-ttu-id="20ac7-103">Traducción</span><span class="sxs-lookup"><span data-stu-id="20ac7-103">Translation</span></span>

<span data-ttu-id="20ac7-104">Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="20ac7-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="20ac7-105">llamando a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer el espacio universal adecuado en la transformación de espacio en la página.</span><span class="sxs-lookup"><span data-stu-id="20ac7-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="20ac7-106">La función SetWorldTransform recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="20ac7-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="20ac7-107">Los miembros eDx y eDy de XFORM especifican los componentes de traslación horizontal y vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="20ac7-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="20ac7-108">Cuando se produce la *conversión* , cada punto de un objeto se desplaza verticalmente, horizontalmente o ambos en una cantidad especificada.</span><span class="sxs-lookup"><span data-stu-id="20ac7-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="20ac7-109">En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades que se ha traducido a la derecha 10 unidades cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="20ac7-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![Ilustración que muestra un rectángulo en una posición en el espacio del mundo y en una posición diferente en el espacio de la página](images/cstrn-09.png)

<span data-ttu-id="20ac7-111">En la ilustración anterior, la coordenada x de cada punto del rectángulo es de 10 unidades mayor que la coordenada x original.</span><span class="sxs-lookup"><span data-stu-id="20ac7-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="20ac7-112">La traducción horizontal se puede representar mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="20ac7-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="20ac7-113">Donde x es la nueva coordenada x, x es la coordenada x original y DX es la distancia horizontal movida.</span><span class="sxs-lookup"><span data-stu-id="20ac7-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="20ac7-114">La traducción vertical se puede representar mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="20ac7-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="20ac7-115">Donde y ' es la nueva coordenada y, y es la coordenada y original, y DY es la distancia vertical movida.</span><span class="sxs-lookup"><span data-stu-id="20ac7-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="20ac7-116">Las transformaciones de traslación horizontal y vertical se pueden combinar en una sola operación mediante una matriz de 3 por 3.</span><span class="sxs-lookup"><span data-stu-id="20ac7-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="20ac7-117">(Las reglas del estado de multiplicación de matrices que indica que el número de filas de una matriz debe ser igual al número de columnas del otro.</span><span class="sxs-lookup"><span data-stu-id="20ac7-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="20ac7-118">El entero 1 de la matriz \| x y 1 \| es un marcador de posición que se agregó para cumplir este requisito.)</span><span class="sxs-lookup"><span data-stu-id="20ac7-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="20ac7-119">La matriz de 3 por 3 que generó la transformación de traducción ilustrada contiene los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="20ac7-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



