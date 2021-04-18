---
title: estructura de plano (Windowsnumerics. h)
description: Esta estructura representa un plano mediante un vector 3D normal y un valor de distancia.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- estructura del plano
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721609"
---
# <a name="plane-structure"></a><span data-ttu-id="ebc24-104">estructura del plano</span><span class="sxs-lookup"><span data-stu-id="ebc24-104">plane structure</span></span>

<span data-ttu-id="ebc24-105">Esta estructura representa un plano mediante un vector 3D normal y un valor de distancia.</span><span class="sxs-lookup"><span data-stu-id="ebc24-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="ebc24-106">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="ebc24-106">This type is available only in C++.</span></span> <span data-ttu-id="ebc24-107">Su equivalente de .NET es [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ebc24-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="ebc24-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="ebc24-108">Constructors</span></span>

| <span data-ttu-id="ebc24-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebc24-109">Name</span></span> | <span data-ttu-id="ebc24-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebc24-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="ebc24-111">Crea un plano no inicializado.</span><span class="sxs-lookup"><span data-stu-id="ebc24-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="ebc24-112">Crea un plano con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="ebc24-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="ebc24-113">Crea un plano a partir de un float3 y una distancia.</span><span class="sxs-lookup"><span data-stu-id="ebc24-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="ebc24-114">Crea un plano a partir de una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ebc24-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="ebc24-115">Convierte un **Microsoft. Graphics. Canvas. Numerics. Plane** en un plano.</span><span class="sxs-lookup"><span data-stu-id="ebc24-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="ebc24-116">Functions</span><span class="sxs-lookup"><span data-stu-id="ebc24-116">Functions</span></span>

| <span data-ttu-id="ebc24-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebc24-117">Name</span></span> | <span data-ttu-id="ebc24-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebc24-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="ebc24-119">Crea un plano a partir de un conjunto de tres posiciones de vértice, que deben ser diferentes y no en una línea recta.</span><span class="sxs-lookup"><span data-stu-id="ebc24-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="ebc24-120">Cambia los coeficientes del vector normal de un plano para que sea de longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="ebc24-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="ebc24-121">Transforma un plano normalizado mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="ebc24-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="ebc24-122">Transforma un plano normalizado mediante una rotación de cuaternión.</span><span class="sxs-lookup"><span data-stu-id="ebc24-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="ebc24-123">Calcula el producto escalar de un plano con un vector.</span><span class="sxs-lookup"><span data-stu-id="ebc24-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="ebc24-124">Calcula el producto escalar de un plano con una coordenada float3.</span><span class="sxs-lookup"><span data-stu-id="ebc24-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="ebc24-125">A diferencia \_ de DOT normal, este cálculo incluye el valor de plano d.</span><span class="sxs-lookup"><span data-stu-id="ebc24-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="ebc24-126">Calcula el producto escalar de un plano con un float3 normal.</span><span class="sxs-lookup"><span data-stu-id="ebc24-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="ebc24-127">A diferencia \_ de la coordenada de puntos, este cálculo omite el valor de plano d.</span><span class="sxs-lookup"><span data-stu-id="ebc24-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="ebc24-128">Operadores</span><span class="sxs-lookup"><span data-stu-id="ebc24-128">Operators</span></span>

| <span data-ttu-id="ebc24-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebc24-129">Name</span></span> | <span data-ttu-id="ebc24-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebc24-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="ebc24-131">Determina si dos instancias de plano son iguales.</span><span class="sxs-lookup"><span data-stu-id="ebc24-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="ebc24-132">Determina si dos instancias de plano no son iguales.</span><span class="sxs-lookup"><span data-stu-id="ebc24-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="ebc24-133">Convierte un plano en un **Microsoft. Graphics. Canvas. Numerics. Plane**.</span><span class="sxs-lookup"><span data-stu-id="ebc24-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="ebc24-134">Campos</span><span class="sxs-lookup"><span data-stu-id="ebc24-134">Fields</span></span>

| <span data-ttu-id="ebc24-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebc24-135">Name</span></span> | <span data-ttu-id="ebc24-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebc24-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="ebc24-137">Vector normal del plano.</span><span class="sxs-lookup"><span data-stu-id="ebc24-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="ebc24-138">Distancia del plano a lo largo de su normal desde el origen.</span><span class="sxs-lookup"><span data-stu-id="ebc24-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ebc24-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebc24-139">Requirements</span></span>

| <span data-ttu-id="ebc24-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc24-140">Requirement</span></span> | <span data-ttu-id="ebc24-141">Value</span><span class="sxs-lookup"><span data-stu-id="ebc24-141">Value</span></span> |
|-|-|
| <span data-ttu-id="ebc24-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebc24-142">Namespace</span></span> | <span data-ttu-id="ebc24-143">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="ebc24-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="ebc24-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebc24-144">Header</span></span> | <dl> <span data-ttu-id="ebc24-145"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc24-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ebc24-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebc24-146">See also</span></span>

[<span data-ttu-id="ebc24-147">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="ebc24-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
