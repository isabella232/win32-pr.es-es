---
title: estructura float3 (Windowsnumerics. h)
description: Vector con tres componentes.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- estructura float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721618"
---
# <a name="float3-structure"></a><span data-ttu-id="8f40e-104">estructura float3</span><span class="sxs-lookup"><span data-stu-id="8f40e-104">float3 structure</span></span>

<span data-ttu-id="8f40e-105">Vector con tres componentes.</span><span class="sxs-lookup"><span data-stu-id="8f40e-105">A vector with three components.</span></span>

<span data-ttu-id="8f40e-106">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="8f40e-106">This type is available only in C++.</span></span> <span data-ttu-id="8f40e-107">Su equivalente de .NET es [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="8f40e-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="8f40e-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="8f40e-108">Constructors</span></span>

| <span data-ttu-id="8f40e-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f40e-109">Name</span></span> | <span data-ttu-id="8f40e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f40e-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="8f40e-111">Crea un float3 no inicializado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="8f40e-112">Crea un float3 con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="8f40e-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="8f40e-113">Crea un float3 con x e y copiados de un float2 más el valor z especificado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="8f40e-114">Crea un float3 con todos los componentes establecidos en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="8f40e-115">Convierte un **Microsoft. Graphics. Canvas. Numerics. Vector3** en un float3.</span><span class="sxs-lookup"><span data-stu-id="8f40e-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="8f40e-116">Functions</span><span class="sxs-lookup"><span data-stu-id="8f40e-116">Functions</span></span>

| <span data-ttu-id="8f40e-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f40e-117">Name</span></span> | <span data-ttu-id="8f40e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f40e-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="8f40e-119">Calcula la longitud o la distancia euclidiana del vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="8f40e-120">Calcula la longitud, o euclidiana, del vector cuadrado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-121">Calcula la distancia euclidiana entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-122">Calcula la distancia euclidiana entre dos vectores con un cuadrado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="8f40e-123">Calcula el producto escalar de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="8f40e-124">Crea un vector de unidad a partir del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="8f40e-125">Calcula el producto vectorial de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="8f40e-126">Determina el vector de reflejo del vector dado y el normal.</span><span class="sxs-lookup"><span data-stu-id="8f40e-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-127">Devuelve un vector que contiene el valor más bajo de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="8f40e-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-128">Devuelve un vector que contiene el valor más alto de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="8f40e-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="8f40e-129">Restringe un valor para que esté dentro de un intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="8f40e-130">Realiza una interpolación lineal entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="8f40e-131">Transforma el vector (x, y, z, 1) de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="8f40e-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="8f40e-132">Transforma el vector normal (x, y, z, 0) de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="8f40e-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="8f40e-133">Transforma un float3 por el cuaternión dado.</span><span class="sxs-lookup"><span data-stu-id="8f40e-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="8f40e-134">Métodos</span><span class="sxs-lookup"><span data-stu-id="8f40e-134">Methods</span></span>

| <span data-ttu-id="8f40e-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f40e-135">Name</span></span> | <span data-ttu-id="8f40e-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f40e-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="8f40e-137">Devuelve un float3 con todos sus componentes establecidos en cero.</span><span class="sxs-lookup"><span data-stu-id="8f40e-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="8f40e-138">Devuelve un float3 con todos sus componentes establecidos en uno.</span><span class="sxs-lookup"><span data-stu-id="8f40e-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="8f40e-139">Devuelve el float3 (1,0).</span><span class="sxs-lookup"><span data-stu-id="8f40e-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="8f40e-140">Devuelve float3 (0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="8f40e-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="8f40e-141">Devuelve float3 (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="8f40e-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="8f40e-142">Operadores</span><span class="sxs-lookup"><span data-stu-id="8f40e-142">Operators</span></span>

| <span data-ttu-id="8f40e-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f40e-143">Name</span></span> | <span data-ttu-id="8f40e-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f40e-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-145">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-146">Resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-147">Multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="8f40e-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="8f40e-148">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8f40e-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="8f40e-149">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8f40e-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-150">Divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="8f40e-151">Divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8f40e-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="8f40e-152">Devuelve un vector que apunta en la dirección opuesta.</span><span class="sxs-lookup"><span data-stu-id="8f40e-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="8f40e-153">En contexto, agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="8f40e-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="8f40e-154">En contexto resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="8f40e-155">En contexto multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="8f40e-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="8f40e-156">En contexto multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8f40e-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="8f40e-157">En contexto divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="8f40e-158">In-Place divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8f40e-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-159">Determina si dos instancias de float3 son iguales.</span><span class="sxs-lookup"><span data-stu-id="8f40e-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="8f40e-160">Determina si dos instancias de float3 no son iguales.</span><span class="sxs-lookup"><span data-stu-id="8f40e-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="8f40e-161">Convierte un float3 en un **Microsoft. Graphics. Canvas. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="8f40e-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="8f40e-162">Campos</span><span class="sxs-lookup"><span data-stu-id="8f40e-162">Fields</span></span>

| <span data-ttu-id="8f40e-163">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f40e-163">Name</span></span> | <span data-ttu-id="8f40e-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f40e-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="8f40e-165">Componente X del vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="8f40e-166">Componente Y del vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="8f40e-167">Componente Z del vector.</span><span class="sxs-lookup"><span data-stu-id="8f40e-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="8f40e-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f40e-168">Requirements</span></span>

| <span data-ttu-id="8f40e-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f40e-169">Requirement</span></span> | <span data-ttu-id="8f40e-170">Value</span><span class="sxs-lookup"><span data-stu-id="8f40e-170">Value</span></span> |
|-|-|
| <span data-ttu-id="8f40e-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f40e-171">Namespace</span></span> | <span data-ttu-id="8f40e-172">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="8f40e-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="8f40e-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f40e-173">Header</span></span> | <dl> <span data-ttu-id="8f40e-174"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f40e-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8f40e-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f40e-175">See also</span></span>

[<span data-ttu-id="8f40e-176">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="8f40e-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
