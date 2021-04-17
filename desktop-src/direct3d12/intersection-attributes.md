---
title: Estructura de atributos de intersección
description: Estructura declarada en HLSL que representa los atributos de acierto para la intersección de triángulo de función fija o el rectángulo de selección alineado con el eje para la intersección de primitiva de procedimiento.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105717339"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="4bb00-103">Estructura de atributos de intersección</span><span class="sxs-lookup"><span data-stu-id="4bb00-103">Intersection attributes structure</span></span> 

<span data-ttu-id="4bb00-104">Estructura declarada en HLSL que representa los atributos de acierto para la intersección de triángulo de función fija o el rectángulo de selección alineado con el eje para la intersección de primitiva de procedimiento.</span><span class="sxs-lookup"><span data-stu-id="4bb00-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="4bb00-105">Intersección de triángulo de función fija</span><span class="sxs-lookup"><span data-stu-id="4bb00-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="4bb00-106">La siguiente estructura se declara en HLSL para representar los atributos de acierto para la intersección de triangulación de función fija:</span><span class="sxs-lookup"><span data-stu-id="4bb00-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="4bb00-107">[Cualquier posicionamiento](any-hit-shader.md) y sombreadores de [posicionamiento más cercanos](closest-hit-shader.md) invocados mediante la intersección de triángulo de función fija debe utilizar esta estructura para los atributos de acceso.</span><span class="sxs-lookup"><span data-stu-id="4bb00-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="4bb00-108">Determinados atributos a0, a1 y a2 para los 3 vértices de un triángulo, barycentrics. x es el peso de a1 y barycentrics. y es el peso de a2.</span><span class="sxs-lookup"><span data-stu-id="4bb00-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="4bb00-109">Por ejemplo, la aplicación puede interpolar haciendo lo siguiente: a = a0 + barycentrics. x \* (a1-a0) + barycentrics. y \* (a2 – a0).</span><span class="sxs-lookup"><span data-stu-id="4bb00-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="4bb00-110">Cuadro de límite alineado con el eje para la intersección de primitiva de procedimiento</span><span class="sxs-lookup"><span data-stu-id="4bb00-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="4bb00-111">Cuando se usan cuadros de límite alineados con el eje para la intersección con primitivas de procedimiento, se desencadena un sombreador de intersección.</span><span class="sxs-lookup"><span data-stu-id="4bb00-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="4bb00-112">Ese sombreador proporciona una estructura de atributo de intersección definida por el usuario a la llamada [**ReportHit**](reporthit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb00-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="4bb00-113">Los sombreadores de aciertos y de posicionamiento más cercanos enlazados al mismo grupo de visitas con este sombreador de intersección deben usar la misma estructura para los atributos de aciertos, incluso si no se hace referencia a los atributos.</span><span class="sxs-lookup"><span data-stu-id="4bb00-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="4bb00-114">El tamaño máximo de la estructura de atributo es de 32 bytes, definido como **D3D12 \_ RAYTRACING \_ Max \_ Attribute \_ size \_ en \_ bytes**.</span><span class="sxs-lookup"><span data-stu-id="4bb00-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


