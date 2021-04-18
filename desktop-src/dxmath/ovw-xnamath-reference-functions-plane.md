---
description: Muestra las funciones de plano proporcionadas por DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funciones de plano de la biblioteca de DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705947"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="804b4-103">Funciones de plano de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="804b4-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="804b4-104">Muestra las funciones de plano proporcionadas por DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="804b4-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="804b4-105">Estas funciones usan un vector de XMVECTOR 4 para representar los coeficientes de la ecuación de plano, AX + by + cz + D = 0, donde el componente X es un, el componente Y es B, el componente Z es C y el componente W es D.</span><span class="sxs-lookup"><span data-stu-id="804b4-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="804b4-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="804b4-106">In this section</span></span>



| <span data-ttu-id="804b4-107">Tema</span><span class="sxs-lookup"><span data-stu-id="804b4-107">Topic</span></span>                                                               | <span data-ttu-id="804b4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="804b4-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="804b4-109">**XMPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="804b4-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="804b4-110">Calcula el producto escalar entre un plano de entrada y un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="804b4-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="804b4-111">**XMPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="804b4-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="804b4-112">Calcula el producto escalar entre un plano de entrada y un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="804b4-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="804b4-113">**XMPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="804b4-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="804b4-114">Calcula el producto de punto entre el vector normal de un plano y un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="804b4-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="804b4-115">**XMPlaneEqual**</span><span class="sxs-lookup"><span data-stu-id="804b4-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="804b4-116">Determina si dos planos son iguales.</span><span class="sxs-lookup"><span data-stu-id="804b4-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="804b4-117">**XMPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="804b4-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="804b4-118">Calcula la ecuación de un plano construido a partir de un punto del plano y un vector normal.</span><span class="sxs-lookup"><span data-stu-id="804b4-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="804b4-119">**XMPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="804b4-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="804b4-120">Calcula la ecuación de un plano construido a partir de tres puntos del plano.</span><span class="sxs-lookup"><span data-stu-id="804b4-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="804b4-121">**XMPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="804b4-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="804b4-122">Busca la intersección entre un plano y una línea.</span><span class="sxs-lookup"><span data-stu-id="804b4-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="804b4-123">**XMPlaneIntersectPlane**</span><span class="sxs-lookup"><span data-stu-id="804b4-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="804b4-124">Busca la intersección de dos planos.</span><span class="sxs-lookup"><span data-stu-id="804b4-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="804b4-125">**XMPlaneIsInfinite**</span><span class="sxs-lookup"><span data-stu-id="804b4-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="804b4-126">Comprueba si alguno de los coeficientes de un plano es infinito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="804b4-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="804b4-127">**XMPlaneIsNaN**</span><span class="sxs-lookup"><span data-stu-id="804b4-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="804b4-128">Comprueba si alguno de los coeficientes de un plano es un NaN.</span><span class="sxs-lookup"><span data-stu-id="804b4-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="804b4-129">**XMPlaneNearEqual**</span><span class="sxs-lookup"><span data-stu-id="804b4-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="804b4-130">Determina si dos planos son casi iguales.</span><span class="sxs-lookup"><span data-stu-id="804b4-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="804b4-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="804b4-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="804b4-132">Normaliza los coeficientes de un plano para que los coeficientes de x, y y z formen un vector normal de unidad.</span><span class="sxs-lookup"><span data-stu-id="804b4-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="804b4-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="804b4-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="804b4-134">Calcula los coeficientes de un plano de modo que los coeficientes de x, y y z formen un vector normal de unidad.</span><span class="sxs-lookup"><span data-stu-id="804b4-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="804b4-135">**XMPlaneNotEqual**</span><span class="sxs-lookup"><span data-stu-id="804b4-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="804b4-136">Determina si dos planos no son iguales.</span><span class="sxs-lookup"><span data-stu-id="804b4-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="804b4-137">**XMPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="804b4-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="804b4-138">Transforma un plano por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="804b4-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="804b4-139">**XMPlaneTransformStream**</span><span class="sxs-lookup"><span data-stu-id="804b4-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="804b4-140">Transforma una secuencia de planos por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="804b4-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="804b4-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="804b4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="804b4-142">Funciones de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="804b4-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
