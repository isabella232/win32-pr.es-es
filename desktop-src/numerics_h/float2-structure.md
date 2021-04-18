---
title: estructura float2 (Windowsnumerics. h)
description: Vector con dos componentes.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- estructura float2
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721619"
---
# <a name="float2-structure"></a><span data-ttu-id="f4429-104">estructura float2</span><span class="sxs-lookup"><span data-stu-id="f4429-104">float2 structure</span></span>

<span data-ttu-id="f4429-105">Vector con dos componentes.</span><span class="sxs-lookup"><span data-stu-id="f4429-105">A vector with two components.</span></span>

<span data-ttu-id="f4429-106">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="f4429-106">This type is available only in C++.</span></span> <span data-ttu-id="f4429-107">Su equivalente de .NET es [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="f4429-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="f4429-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="f4429-108">Constructors</span></span>

| <span data-ttu-id="f4429-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4429-109">Name</span></span> | <span data-ttu-id="f4429-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4429-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="f4429-111">Crea un float2 no inicializado.</span><span class="sxs-lookup"><span data-stu-id="f4429-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="f4429-112">Crea un float2 con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="f4429-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="f4429-113">Crea un float2 con todos los componentes establecidos en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f4429-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="f4429-114">Convierte un **Microsoft. Graphics. Canvas. Numerics. Vector2** en un float2.</span><span class="sxs-lookup"><span data-stu-id="f4429-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="f4429-115">Convierte un [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) en un float2.</span><span class="sxs-lookup"><span data-stu-id="f4429-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="f4429-116">Convierte un de [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) en un float2.</span><span class="sxs-lookup"><span data-stu-id="f4429-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="f4429-117">Functions</span><span class="sxs-lookup"><span data-stu-id="f4429-117">Functions</span></span>

| <span data-ttu-id="f4429-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4429-118">Name</span></span> | <span data-ttu-id="f4429-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4429-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="f4429-120">Calcula la longitud o la distancia euclidiana del vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="f4429-121">Calcula la longitud, o euclidiana, del vector cuadrado.</span><span class="sxs-lookup"><span data-stu-id="f4429-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-122">Calcula la distancia euclidiana entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="f4429-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-123">Calcula la distancia euclidiana entre dos vectores con un cuadrado.</span><span class="sxs-lookup"><span data-stu-id="f4429-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-124">Calcula el producto escalar de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="f4429-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="f4429-125">Crea un vector de unidad a partir del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="f4429-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="f4429-126">Determina el vector de reflejo del vector dado y el normal.</span><span class="sxs-lookup"><span data-stu-id="f4429-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-127">Devuelve un vector que contiene el valor más bajo de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="f4429-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-128">Devuelve un vector que contiene el valor más alto de cada par coincidente de componentes.</span><span class="sxs-lookup"><span data-stu-id="f4429-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="f4429-129">Restringe un valor para que esté dentro de un intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="f4429-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="f4429-130">Realiza una interpolación lineal entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="f4429-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="f4429-131">Transforma el vector (x, y, 0, 1) por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="f4429-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="f4429-132">Transforma el vector (x, y, 0, 1) por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="f4429-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="f4429-133">Transforma el vector normal (x, y, 0, 0) de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="f4429-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="f4429-134">Transforma el vector normal (x, y, 0, 0) de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="f4429-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="f4429-135">Transforma un float2 por el cuaternión dado.</span><span class="sxs-lookup"><span data-stu-id="f4429-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="f4429-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="f4429-136">Methods</span></span>

| <span data-ttu-id="f4429-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4429-137">Name</span></span> | <span data-ttu-id="f4429-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4429-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="f4429-139">Devuelve un float2 con todos sus componentes establecidos en cero.</span><span class="sxs-lookup"><span data-stu-id="f4429-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="f4429-140">Devuelve un float2 con todos sus componentes establecidos en uno.</span><span class="sxs-lookup"><span data-stu-id="f4429-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="f4429-141">Devuelve el float2 (1,0).</span><span class="sxs-lookup"><span data-stu-id="f4429-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="f4429-142">Devuelve float2 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="f4429-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="f4429-143">Operadores</span><span class="sxs-lookup"><span data-stu-id="f4429-143">Operators</span></span>

| <span data-ttu-id="f4429-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4429-144">Name</span></span> | <span data-ttu-id="f4429-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4429-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="f4429-146">Convierte un float2 en [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="f4429-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="f4429-147">Convierte un float2 en [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="f4429-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-148">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="f4429-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-149">Resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-150">Multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="f4429-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="f4429-151">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="f4429-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="f4429-152">Multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="f4429-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-153">Divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="f4429-154">Divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="f4429-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="f4429-155">Devuelve un vector que apunta en la dirección opuesta.</span><span class="sxs-lookup"><span data-stu-id="f4429-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="f4429-156">En contexto, agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="f4429-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="f4429-157">En contexto resta un vector de un vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="f4429-158">En contexto multiplica los componentes de dos vectores entre sí.</span><span class="sxs-lookup"><span data-stu-id="f4429-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="f4429-159">En contexto multiplica un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="f4429-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="f4429-160">En contexto divide los componentes de un vector por los componentes de otro vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="f4429-161">In-Place divide un vector por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="f4429-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-162">Determina si dos instancias de float2 son iguales.</span><span class="sxs-lookup"><span data-stu-id="f4429-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="f4429-163">Determina si dos instancias de float2 no son iguales.</span><span class="sxs-lookup"><span data-stu-id="f4429-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="f4429-164">Convierte un float2 en **Microsoft. Graphics. Canvas. Numerics. Vector2**.</span><span class="sxs-lookup"><span data-stu-id="f4429-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="f4429-165">Campos</span><span class="sxs-lookup"><span data-stu-id="f4429-165">Fields</span></span>

| <span data-ttu-id="f4429-166">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4429-166">Name</span></span> | <span data-ttu-id="f4429-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4429-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="f4429-168">Componente X del vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="f4429-169">Componente Y del vector.</span><span class="sxs-lookup"><span data-stu-id="f4429-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="f4429-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4429-170">Requirements</span></span>

| <span data-ttu-id="f4429-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4429-171">Requirement</span></span> | <span data-ttu-id="f4429-172">Value</span><span class="sxs-lookup"><span data-stu-id="f4429-172">Value</span></span> |
|-|-|
| <span data-ttu-id="f4429-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4429-173">Namespace</span></span> | <span data-ttu-id="f4429-174">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="f4429-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="f4429-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4429-175">Header</span></span> | <dl> <span data-ttu-id="f4429-176"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4429-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="f4429-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4429-177">See also</span></span>

[<span data-ttu-id="f4429-178">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="f4429-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
