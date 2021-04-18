---
title: FLOAT4 (estructura) (Windowsnumerics. h)
description: Vector con cuatro componentes.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- FLOAT4 (estructura)
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721611"
---
# <a name="float4-structure"></a><span data-ttu-id="ccbbf-104">FLOAT4 (estructura)</span><span class="sxs-lookup"><span data-stu-id="ccbbf-104">float4 structure</span></span>

<span data-ttu-id="ccbbf-105">Vector con cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-105">A vector with four components.</span></span>

<span data-ttu-id="ccbbf-106">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-106">This type is available only in C++.</span></span> <span data-ttu-id="ccbbf-107">Su equivalente de .NET es [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ccbbf-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="ccbbf-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="ccbbf-108">Constructors</span></span>

| <span data-ttu-id="ccbbf-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccbbf-109">Name</span></span> | <span data-ttu-id="ccbbf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccbbf-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="ccbbf-111">Crea un FLOAT4 no inicializado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="ccbbf-112">Crea un FLOAT4 con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="ccbbf-113">Crea un FLOAT4 con x e y copiados de un float2 más los valores z y w especificados.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="ccbbf-114">Crea un FLOAT4 con x, y y z copiados de un float3 más el valor de w especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="ccbbf-115">Crea un FLOAT4 con todos los com. entes establecidos en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="ccbbf-116">Convierte un **Microsoft. Graphics. Canvas. Numerics. Vector4** en FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="ccbbf-117">Functions</span><span class="sxs-lookup"><span data-stu-id="ccbbf-117">Functions</span></span>

| <span data-ttu-id="ccbbf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccbbf-118">Name</span></span> | <span data-ttu-id="ccbbf-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccbbf-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="ccbbf-120">Calcula la longitud o la distancia euclidiana del vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="ccbbf-121">Calcula la longitud, o euclidiana, del vector cuadrado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-122">Calcula la distancia euclidiana entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-123">Calcula la distancia euclidiana entre dos vectores con un cuadrado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="ccbbf-124">Calcula el producto escalar de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="ccbbf-125">Crea un vector de unidad a partir del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-126">Devuelve un vector que contiene el valor más bajo de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-127">Devuelve un vector que contiene el valor más alto de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="ccbbf-128">Restringe un valor para que esté dentro de un intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="ccbbf-129">Realiza una interpolación lineal entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="ccbbf-130">Transforma una FLOAT4 en la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="ccbbf-131">Transforma un float3 por la matriz especificada y devuelve una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="ccbbf-132">Transforma un float2 por la matriz especificada y devuelve una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="ccbbf-133">Transforma un FLOAT4 por el cuaternión especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="ccbbf-134">Transforma un float3 por el cuaternión dado y devuelve una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="ccbbf-135">Transforma un float2 por el cuaternión dado y devuelve una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="ccbbf-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="ccbbf-136">Methods</span></span>

| <span data-ttu-id="ccbbf-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccbbf-137">Name</span></span> | <span data-ttu-id="ccbbf-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccbbf-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="ccbbf-139">Devuelve un FLOAT4 con todos sus componentes establecidos en cero.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="ccbbf-140">Devuelve un FLOAT4 con todos sus componentes establecidos en uno.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="ccbbf-141">Devuelve FLOAT4 (1, 0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ccbbf-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="ccbbf-142">Devuelve la FLOAT4 (0, 1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ccbbf-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="ccbbf-143">Devuelve el valor de FLOAT4 (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="ccbbf-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="ccbbf-144">Devuelve la FLOAT4 (0,0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="ccbbf-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="ccbbf-145">Operadores</span><span class="sxs-lookup"><span data-stu-id="ccbbf-145">Operators</span></span>

| <span data-ttu-id="ccbbf-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccbbf-146">Name</span></span> | <span data-ttu-id="ccbbf-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccbbf-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-148">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-149">Resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-150">Multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="ccbbf-151">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="ccbbf-152">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-153">Divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="ccbbf-154">Divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="ccbbf-155">Devuelve un vector que apunta en la dirección opuesta.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-156">En contexto, agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-157">En contexto resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-158">En contexto multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="ccbbf-159">En contexto multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-160">En contexto divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="ccbbf-161">In-Place divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-162">Determina si dos instancias de FLOAT4 son iguales.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="ccbbf-163">Determina si dos instancias de FLOAT4 no son iguales.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="ccbbf-164">Convierte un FLOAT4 en un **Microsoft. Graphics. Canvas. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="ccbbf-165">Campos</span><span class="sxs-lookup"><span data-stu-id="ccbbf-165">Fields</span></span>

| <span data-ttu-id="ccbbf-166">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccbbf-166">Name</span></span> | <span data-ttu-id="ccbbf-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccbbf-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="ccbbf-168">Componente X del vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="ccbbf-169">Componente Y del vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="ccbbf-170">Componente Z del vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="ccbbf-171">Componente W del vector.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ccbbf-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccbbf-172">Requirements</span></span>

| <span data-ttu-id="ccbbf-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccbbf-173">Requirement</span></span> | <span data-ttu-id="ccbbf-174">Value</span><span class="sxs-lookup"><span data-stu-id="ccbbf-174">Value</span></span> |
|-|-|
| <span data-ttu-id="ccbbf-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccbbf-175">Namespace</span></span> | <span data-ttu-id="ccbbf-176">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="ccbbf-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="ccbbf-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccbbf-177">Header</span></span> | <dl> <span data-ttu-id="ccbbf-178"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccbbf-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ccbbf-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccbbf-179">See also</span></span>

[<span data-ttu-id="ccbbf-180">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="ccbbf-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
