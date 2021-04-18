---
title: estructura float3x2 (Windowsnumerics. h)
description: Matriz 3x2, que se usa para las transformaciones 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- estructura float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721617"
---
# <a name="float3x2-structure"></a><span data-ttu-id="53979-104">estructura float3x2</span><span class="sxs-lookup"><span data-stu-id="53979-104">float3x2 structure</span></span>

<span data-ttu-id="53979-105">Matriz 3x2, que se usa para las transformaciones 2D.</span><span class="sxs-lookup"><span data-stu-id="53979-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="53979-106">Este tipo de matriz utiliza un diseño de vector de fila.</span><span class="sxs-lookup"><span data-stu-id="53979-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="53979-107">Los valores x e y del vector de conversión de esta matriz se corresponden con los campos M31, M32.</span><span class="sxs-lookup"><span data-stu-id="53979-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="53979-108">Este tipo solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="53979-108">This type is available only in C++.</span></span> <span data-ttu-id="53979-109">Su equivalente de .NET es [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="53979-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="53979-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="53979-110">Constructors</span></span>

| <span data-ttu-id="53979-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="53979-111">Name</span></span> | <span data-ttu-id="53979-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="53979-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="53979-113">Crea un float3x2 no inicializado.</span><span class="sxs-lookup"><span data-stu-id="53979-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="53979-114">Crea un float3x2 con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="53979-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="53979-115">Convierte un **Microsoft. Graphics. Canvas. Numerics. Matrix3x2** en float3x2.</span><span class="sxs-lookup"><span data-stu-id="53979-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="53979-116">Functions</span><span class="sxs-lookup"><span data-stu-id="53979-116">Functions</span></span>

| <span data-ttu-id="53979-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="53979-117">Name</span></span> | <span data-ttu-id="53979-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="53979-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="53979-119">Crea una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="53979-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="53979-120">Crea una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="53979-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="53979-121">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="53979-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="53979-122">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="53979-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="53979-123">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="53979-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="53979-124">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="53979-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="53979-125">Crea una matriz de escala, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="53979-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="53979-126">Crea una matriz de escala, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="53979-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="53979-127">Crea una matriz de sesgo, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="53979-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="53979-128">Crea una matriz de sesgo, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="53979-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="53979-129">Crea una matriz de rotación, centrada en el origen.</span><span class="sxs-lookup"><span data-stu-id="53979-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="53979-130">Crea una matriz de rotación, centrada en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="53979-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="53979-131">Comprueba si se trata de una matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="53979-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="53979-132">Calcula el factor determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="53979-133">Obtiene el vector de traslación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="53979-134">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="53979-135">Devuelve true si se puede invertir la matriz; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="53979-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="53979-136">Interpola linealmente entre los valores correspondientes de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="53979-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="53979-137">Métodos</span><span class="sxs-lookup"><span data-stu-id="53979-137">Methods</span></span>

| <span data-ttu-id="53979-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="53979-138">Name</span></span> | <span data-ttu-id="53979-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="53979-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="53979-140">Devuelve una instancia de la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="53979-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="53979-141">Operadores</span><span class="sxs-lookup"><span data-stu-id="53979-141">Operators</span></span>

| <span data-ttu-id="53979-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="53979-142">Name</span></span> | <span data-ttu-id="53979-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="53979-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="53979-144">Agrega cada componente de una matriz a otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="53979-145">Resta todos los componentes de una matriz de otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="53979-146">Multiplica una matriz por otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="53979-147">Esto tiene el efecto de concatenar dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="53979-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="53979-148">Multiplica cada componente de una matriz por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="53979-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="53979-149">Niega cada componente de una matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="53979-150">En contexto agrega cada componente de una matriz a otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="53979-151">En contexto resta cada componente de una matriz de otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="53979-152">En contexto multiplica una matriz por otra matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="53979-153">Esto tiene el efecto de concatenar dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="53979-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="53979-154">En contexto multiplica cada componente de una matriz por un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="53979-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="53979-155">Determina si dos instancias de float3x2 son iguales.</span><span class="sxs-lookup"><span data-stu-id="53979-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="53979-156">Determina si dos instancias de float3x2 no son iguales.</span><span class="sxs-lookup"><span data-stu-id="53979-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="53979-157">Convierte un float3x2 en **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="53979-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="53979-158">Campos</span><span class="sxs-lookup"><span data-stu-id="53979-158">Fields</span></span>

| <span data-ttu-id="53979-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="53979-159">Name</span></span> | <span data-ttu-id="53979-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="53979-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="53979-161">Valor de la fila 1 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="53979-162">Valor de la fila 1 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="53979-163">Valor de la fila 2 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="53979-164">Valor de la fila 2 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="53979-165">Valor de la fila 3 columna 1 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="53979-166">Valor de la fila 3 columna 2 de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53979-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="53979-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53979-167">Requirements</span></span>

| <span data-ttu-id="53979-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="53979-168">Requirement</span></span> | <span data-ttu-id="53979-169">Value</span><span class="sxs-lookup"><span data-stu-id="53979-169">Value</span></span> |
|-|-|
| <span data-ttu-id="53979-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53979-170">Namespace</span></span> | <span data-ttu-id="53979-171">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="53979-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="53979-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53979-172">Header</span></span> | <dl> <span data-ttu-id="53979-173"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="53979-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="53979-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="53979-174">See also</span></span>

[<span data-ttu-id="53979-175">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="53979-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
