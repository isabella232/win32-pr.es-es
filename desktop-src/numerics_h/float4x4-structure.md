---
title: estructura float4x4 (Windowsnumerics. h)
description: Matriz 4x4 utilizada para las transformaciones 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- estructura float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721610"
---
# <a name="float4x4-structure"></a><span data-ttu-id="5528f-104">estructura float4x4</span><span class="sxs-lookup"><span data-stu-id="5528f-104">float4x4 structure</span></span>

<span data-ttu-id="5528f-105">Matriz 4x4 utilizada para las transformaciones 3D.</span><span class="sxs-lookup"><span data-stu-id="5528f-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="5528f-106">Este tipo de matriz utiliza un diseño de vector de fila.</span><span class="sxs-lookup"><span data-stu-id="5528f-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="5528f-107">Los valores x, y y z del vector de conversión de esta matriz se corresponden con los campos M41, M42, M43.</span><span class="sxs-lookup"><span data-stu-id="5528f-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="5528f-108">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="5528f-108">This type is available only in C++.</span></span> <span data-ttu-id="5528f-109">Su equivalente de .NET es [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="5528f-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="5528f-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="5528f-110">Constructors</span></span>

| <span data-ttu-id="5528f-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5528f-111">Name</span></span> | <span data-ttu-id="5528f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5528f-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="5528f-113">Crea un float4x4 no inicializado.</span><span class="sxs-lookup"><span data-stu-id="5528f-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="5528f-114">Crea un float4x4 con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="5528f-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="5528f-115">Crea un float4x4 a partir de un float3x2.</span><span class="sxs-lookup"><span data-stu-id="5528f-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="5528f-116">Convierte un **Microsoft. Graphics. Canvas. Numerics. Matrix4x4** en float4x4.</span><span class="sxs-lookup"><span data-stu-id="5528f-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="5528f-117">Functions</span><span class="sxs-lookup"><span data-stu-id="5528f-117">Functions</span></span>

| <span data-ttu-id="5528f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="5528f-118">Name</span></span> | <span data-ttu-id="5528f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5528f-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="5528f-120">Crea una cartelera esférica que gira en torno a la posición de un objeto especificado, utilizando un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="5528f-121">Crea una cartelera cilíndrica que gira en torno a un eje especificado, utilizando un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="5528f-122">Crea una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="5528f-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="5528f-123">Crea una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="5528f-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="5528f-124">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="5528f-125">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="5528f-126">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="5528f-127">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="5528f-128">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="5528f-129">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="5528f-130">Crea una matriz de rotación del eje x, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="5528f-131">Crea una matriz de rotación del eje x, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="5528f-132">Crea una matriz de rotación del eje y, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="5528f-133">Crea una matriz de rotación del eje y, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="5528f-134">Crea una matriz de rotación del eje z, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="5528f-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="5528f-135">Crea una matriz de rotación del eje z, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="5528f-136">Crea una matriz que gira en torno a un vector arbitrario.</span><span class="sxs-lookup"><span data-stu-id="5528f-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="5528f-137">Crea una matriz de proyección en perspectiva basada en un campo de vista, utilizando un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="5528f-138">Crea una matriz de proyección en perspectiva con un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="5528f-139">Crea una matriz de proyección en perspectiva personalizada mediante un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="5528f-140">Crea una matriz de proyección ortográfica mediante un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="5528f-141">Crea una matriz de proyección ortográfica personalizada mediante un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="5528f-142">Crea una matriz de vista mediante un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="5528f-143">Crea una matriz universal mediante un sistema de coordenadas de la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="5528f-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="5528f-144">Se puede usar para colocar objetos en el espacio 3D.</span><span class="sxs-lookup"><span data-stu-id="5528f-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="5528f-145">Crea una matriz de rotación a partir de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="5528f-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="5528f-146">Crea una matriz de rotación a partir de una guiñada, un tono y un rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="5528f-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="5528f-147">Crea una matriz que aplana la geometría en un plano especificado como si proyectara una sombra desde una fuente de luz especificada.</span><span class="sxs-lookup"><span data-stu-id="5528f-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="5528f-148">Crea una matriz que refleja el sistema de coordenadas sobre un plano especificado.</span><span class="sxs-lookup"><span data-stu-id="5528f-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="5528f-149">Comprueba si se trata de una matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="5528f-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="5528f-150">Calcula el factor determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="5528f-151">Obtiene el vector de traslación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="5528f-152">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="5528f-153">Devuelve true si se puede invertir la matriz; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="5528f-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="5528f-154">Extrae los componentes escalar, traslación y rotación de una matriz de escala 3D/giro/traslación (SRT).</span><span class="sxs-lookup"><span data-stu-id="5528f-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="5528f-155">Devuelve true si la matriz se puede descomponer; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="5528f-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="5528f-156">Transforma una matriz aplicando una rotación de cuaternión.</span><span class="sxs-lookup"><span data-stu-id="5528f-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="5528f-157">Transpone los componentes de una matriz a lo largo de su diagonal.</span><span class="sxs-lookup"><span data-stu-id="5528f-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="5528f-158">Interpola linealmente entre los valores correspondientes de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="5528f-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="5528f-159">Métodos</span><span class="sxs-lookup"><span data-stu-id="5528f-159">Methods</span></span>

| <span data-ttu-id="5528f-160">Nombre</span><span class="sxs-lookup"><span data-stu-id="5528f-160">Name</span></span> | <span data-ttu-id="5528f-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="5528f-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="5528f-162">Devuelve una instancia de la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="5528f-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="5528f-163">Operadores</span><span class="sxs-lookup"><span data-stu-id="5528f-163">Operators</span></span>

| <span data-ttu-id="5528f-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="5528f-164">Name</span></span> | <span data-ttu-id="5528f-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="5528f-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-166">Agrega cada componente de una matriz a otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-167">Resta todos los componentes de una matriz de otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-168">Multiplica una matriz por otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="5528f-169">Esto tiene el efecto de concatenar dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="5528f-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="5528f-170">Multiplica cada componente de una matriz por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="5528f-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="5528f-171">Niega cada componente de una matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-172">En contexto agrega cada componente de una matriz a otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-173">En contexto resta cada componente de una matriz de otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-174">En contexto multiplica una matriz por otra matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="5528f-175">Esto tiene el efecto de concatenar dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="5528f-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="5528f-176">En contexto multiplica cada componente de una matriz por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="5528f-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-177">Determina si dos instancias de float4x4 son iguales.</span><span class="sxs-lookup"><span data-stu-id="5528f-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="5528f-178">Determina si dos instancias de float4x4 no son iguales.</span><span class="sxs-lookup"><span data-stu-id="5528f-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="5528f-179">Convierte un float4x4 en **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**.</span><span class="sxs-lookup"><span data-stu-id="5528f-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="5528f-180">Campos</span><span class="sxs-lookup"><span data-stu-id="5528f-180">Fields</span></span>

| <span data-ttu-id="5528f-181">Nombre</span><span class="sxs-lookup"><span data-stu-id="5528f-181">Name</span></span> | <span data-ttu-id="5528f-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="5528f-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="5528f-183">Valor de la fila 1 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="5528f-184">Valor de la fila 1 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="5528f-185">Valor de la fila 1 columna 3 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="5528f-186">Valor de la fila 1 columna 4 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="5528f-187">Valor de la fila 2 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="5528f-188">Valor de la fila 2 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="5528f-189">Valor de la fila 2 columna 3 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="5528f-190">Valor de la fila 2 columna 4 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="5528f-191">Valor de la fila 3 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="5528f-192">Valor de la fila 3 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="5528f-193">Valor de la fila 3 columna 3 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="5528f-194">Valor de la fila 3 columna 4 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="5528f-195">Valor de la fila 4 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="5528f-196">Valor de la fila 4 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="5528f-197">Valor de la fila 4 columna 3 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="5528f-198">Valor de la fila 4 columna 4 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5528f-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="5528f-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5528f-199">Requirements</span></span>

| <span data-ttu-id="5528f-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="5528f-200">Requirement</span></span> | <span data-ttu-id="5528f-201">Value</span><span class="sxs-lookup"><span data-stu-id="5528f-201">Value</span></span> |
|-|-|
| <span data-ttu-id="5528f-202">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5528f-202">Namespace</span></span> | <span data-ttu-id="5528f-203">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="5528f-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="5528f-204">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5528f-204">Header</span></span> | <dl> <span data-ttu-id="5528f-205"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="5528f-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="5528f-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="5528f-206">See also</span></span>

[<span data-ttu-id="5528f-207">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="5528f-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
