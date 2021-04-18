---
title: estructura cuaternión (Windowsnumerics. h)
description: Un vector de cuatro dimensiones, que se usa para representar un giro.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- cuaternión (estructura)
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721608"
---
# <a name="quaternion-structure"></a><span data-ttu-id="e3816-104">cuaternión (estructura)</span><span class="sxs-lookup"><span data-stu-id="e3816-104">quaternion Structure</span></span>

<span data-ttu-id="e3816-105">Un vector de cuatro dimensiones, que se usa para representar un giro.</span><span class="sxs-lookup"><span data-stu-id="e3816-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="e3816-106">Un cuaternión puede girar de forma eficaz un objeto sobre el vector (x, y, z) en el ángulo Theta, donde w = cos (Theta/2).</span><span class="sxs-lookup"><span data-stu-id="e3816-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="e3816-107">Los cuaterniones se suelen usar para la interpolación suave entre dos ángulos y para evitar el problema de bloqueo de gimbal que puede producirse con los ángulos de Euler.</span><span class="sxs-lookup"><span data-stu-id="e3816-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="e3816-108">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="e3816-108">This type is available only in C++.</span></span> <span data-ttu-id="e3816-109">Su equivalente de .NET es [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="e3816-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="e3816-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="e3816-110">Constructors</span></span>

| <span data-ttu-id="e3816-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3816-111">Name</span></span> | <span data-ttu-id="e3816-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3816-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="e3816-113">Crea un cuaternión no inicializado.</span><span class="sxs-lookup"><span data-stu-id="e3816-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="e3816-114">Crea un cuaternión con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="e3816-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="e3816-115">Crea un cuaternión a partir de un float3 y un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="e3816-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="e3816-116">Convierte un **valor de Microsoft. Graphics. Canvas. Numerics. cuaternión** en un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="e3816-117">Functions</span><span class="sxs-lookup"><span data-stu-id="e3816-117">Functions</span></span>

| <span data-ttu-id="e3816-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3816-118">Name</span></span> | <span data-ttu-id="e3816-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3816-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="e3816-120">Crea un cuaternión a partir de un vector y un ángulo para girar sobre el vector.</span><span class="sxs-lookup"><span data-stu-id="e3816-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="e3816-121">Crea un cuaternión a partir de los ángulos de guiñada, de brea y de rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="e3816-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="e3816-122">Crea un cuaternión a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="e3816-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="e3816-123">Comprueba si se trata de un cuaternión de identidad (sin giro).</span><span class="sxs-lookup"><span data-stu-id="e3816-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="e3816-124">Calcula la longitud de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="e3816-125">Calcula la longitud cuadrada de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="e3816-126">Calcula el producto escalar de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="e3816-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="e3816-127">Divide cada componente de un cuaternión por la longitud del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="e3816-128">Calcula el conjugado de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="e3816-129">Calcula el inverso de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="e3816-130">Interpola entre dos cuaterniones mediante la interpolación lineal esférica.</span><span class="sxs-lookup"><span data-stu-id="e3816-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="e3816-131">Interpola linealmente entre dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="e3816-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-132">Concatena dos cuaterniones; el resultado representa el primer giro seguido del segundo giro.</span><span class="sxs-lookup"><span data-stu-id="e3816-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="e3816-133">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3816-133">Methods</span></span>

| <span data-ttu-id="e3816-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3816-134">Name</span></span> | <span data-ttu-id="e3816-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3816-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="e3816-136">Devuelve una instancia del cuaternión de identidad.</span><span class="sxs-lookup"><span data-stu-id="e3816-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="e3816-137">Operadores</span><span class="sxs-lookup"><span data-stu-id="e3816-137">Operators</span></span>

| <span data-ttu-id="e3816-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3816-138">Name</span></span> | <span data-ttu-id="e3816-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3816-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-140">Agrega dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="e3816-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-141">Resta un cuaternión de otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-142">Multiplica un cuaternión por otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="e3816-143">Multiplica un cuaternión por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="e3816-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-144">Divide un cuaternión por otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="e3816-145">Voltea el signo de cada componente del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e3816-146">En contexto agrega dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="e3816-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e3816-147">En contexto resta un cuaternión de otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e3816-148">En contexto multiplica un cuaternión por otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="e3816-149">En contexto, nultiplies un cuaternión por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="e3816-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e3816-150">En contexto divide un cuaternión por otro cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-151">Determina si dos instancias de Quaternion son iguales.</span><span class="sxs-lookup"><span data-stu-id="e3816-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e3816-152">Determina si dos instancias de Quaternion no son iguales.</span><span class="sxs-lookup"><span data-stu-id="e3816-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="e3816-153">Convierte un cuaternión en **Microsoft. Graphics. Canvas. Numerics. Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="e3816-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="e3816-154">Campos</span><span class="sxs-lookup"><span data-stu-id="e3816-154">Fields</span></span>

| <span data-ttu-id="e3816-155">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3816-155">Name</span></span> | <span data-ttu-id="e3816-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3816-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="e3816-157">Valor X del componente de vector del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="e3816-158">Valor Y del componente de vector del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="e3816-159">Valor Z del componente de vector del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="e3816-160">Componente de rotación del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e3816-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e3816-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3816-161">Requirements</span></span>

| <span data-ttu-id="e3816-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3816-162">Requirement</span></span> | <span data-ttu-id="e3816-163">Value</span><span class="sxs-lookup"><span data-stu-id="e3816-163">Value</span></span> |
|-|-|
| <span data-ttu-id="e3816-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e3816-164">Namespace</span></span> | <span data-ttu-id="e3816-165">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="e3816-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="e3816-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3816-166">Header</span></span> | <dl> <span data-ttu-id="e3816-167"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3816-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e3816-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3816-168">See also</span></span>

[<span data-ttu-id="e3816-169">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="e3816-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
