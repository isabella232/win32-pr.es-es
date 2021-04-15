---
description: Muchas aplicaciones de CAD proporcionan características que giran los objetos dibujados en el área de cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985999"
---
# <a name="rotation"></a><span data-ttu-id="de54f-103">Rotación</span><span class="sxs-lookup"><span data-stu-id="de54f-103">Rotation</span></span>

<span data-ttu-id="de54f-104">Muchas aplicaciones de CAD proporcionan características que giran los objetos dibujados en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="de54f-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="de54f-105">Las aplicaciones que incluyen capacidades de rotación utilizan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio mundial adecuado en la página.</span><span class="sxs-lookup"><span data-stu-id="de54f-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="de54f-106">Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="de54f-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="de54f-107">Los miembros eM11, eM12, eM21 y eM22 de XFORM especifican respectivamente, el coseno, el seno, el seno negativo y el coseno del ángulo de rotación.</span><span class="sxs-lookup"><span data-stu-id="de54f-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="de54f-108">Cuando se produce la *rotación* , los puntos que constituyen un objeto se giran con respecto al origen del espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="de54f-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="de54f-109">En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades girado 30 grados cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="de54f-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![Ilustración que muestra dos espacios de coordenadas; cada una tiene un Rectange en una ubicación diferente y con una rotación diferente](images/cstrn-11.png)

<span data-ttu-id="de54f-111">En la ilustración anterior, cada punto del rectángulo se giró 30 grados con respecto al origen del espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="de54f-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="de54f-112">El algoritmo siguiente calcula la nueva coordenada x (x ') de un punto (x, y) que se gira por el ángulo A con respecto al origen del espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="de54f-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="de54f-113">El algoritmo siguiente calcula la coordenada y (y ') de un punto (x, y) que se gira por el ángulo A con respecto al origen.</span><span class="sxs-lookup"><span data-stu-id="de54f-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="de54f-114">Las dos transformaciones de giro se pueden combinar en una matriz de 2 por 2 como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="de54f-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="de54f-115">La matriz de 2 por 2 que generó el giro contiene los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="de54f-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="de54f-116">Derivación del algoritmo de rotación</span><span class="sxs-lookup"><span data-stu-id="de54f-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="de54f-117">Los algoritmos de rotación se basan en la suma de Teorema de trigonometría, lo que indica que la función trigonométrica de una suma de dos ángulos (a1 y a2) se puede expresar en términos de las funciones trigonométricas de los dos ángulos.</span><span class="sxs-lookup"><span data-stu-id="de54f-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="de54f-118">En la ilustración siguiente se muestra un punto p girado en sentido contrario a las agujas del reloj hacia la nueva posición p '.</span><span class="sxs-lookup"><span data-stu-id="de54f-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="de54f-119">Además, muestra dos triángulos formados por una línea dibujada a partir del origen del espacio de coordenadas hasta cada punto y una línea dibujada a partir de cada punto a través del eje x.</span><span class="sxs-lookup"><span data-stu-id="de54f-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![diagrama que muestra el origen, p y p y dos triángulos](images/cstrn-12.png)

<span data-ttu-id="de54f-121">Con trigonometría, la coordenada x del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de a1.</span><span class="sxs-lookup"><span data-stu-id="de54f-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="de54f-122">La coordenada y del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el seno de a1.</span><span class="sxs-lookup"><span data-stu-id="de54f-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="de54f-123">Del mismo modo, la coordenada x del punto p ' se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="de54f-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="de54f-124">Por último, se puede obtener la coordenada y del punto p ' multiplicando la longitud de la hipotenusa h por el seno de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="de54f-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="de54f-125">Con la suma teorema, los algoritmos anteriores se convierten en los siguientes:</span><span class="sxs-lookup"><span data-stu-id="de54f-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="de54f-126">Los algoritmos de rotación de un punto determinado girados por el ángulo a2 se pueden obtener sustituyendo x por cada aparición de (h \* cos a1) y sustituyendo y por cada aparición de (h \* sin a1).</span><span class="sxs-lookup"><span data-stu-id="de54f-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



