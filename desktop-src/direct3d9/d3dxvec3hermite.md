---
description: Realiza una interpolación de spline Hermite, usando los vectores 3D especificados.
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: Función D3DXVec3Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b5609215d0ab56e9d91979d01f996981b2ffcbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708018"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a><span data-ttu-id="dc702-103">Función D3DXVec3Hermite (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dc702-103">D3DXVec3Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="dc702-104">Realiza una interpolación de spline Hermite, usando los vectores 3D especificados.</span><span class="sxs-lookup"><span data-stu-id="dc702-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc702-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc702-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="dc702-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc702-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dc702-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc702-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="dc702-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc702-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc702-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-112">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="dc702-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-113">*PT1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc702-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc702-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-115">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) de origen, un vector tangente.</span><span class="sxs-lookup"><span data-stu-id="dc702-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-116">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc702-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc702-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="dc702-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-119">*PT2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc702-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc702-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-121">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) de origen, un vector tangente.</span><span class="sxs-lookup"><span data-stu-id="dc702-121">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-122">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dc702-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-124">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="dc702-124">Weighting factor.</span></span> <span data-ttu-id="dc702-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="dc702-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc702-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc702-126">Return value</span></span>

<span data-ttu-id="dc702-127">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc702-127">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dc702-128">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la interpolación de la spline de Hermite.</span><span class="sxs-lookup"><span data-stu-id="dc702-128">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc702-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc702-129">Remarks</span></span>

<span data-ttu-id="dc702-130">La función **D3DXVec3Hermite** se interpola desde (positiona, tangenta) hasta (PositionB, tangentB) mediante la interpolación de spline de Hermite.</span><span class="sxs-lookup"><span data-stu-id="dc702-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="dc702-131">La interpolación spline es una generalización de la spline de fácil entrada y de fácil salida.</span><span class="sxs-lookup"><span data-stu-id="dc702-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="dc702-132">La rampa es una función de Q (s) con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc702-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="dc702-133">Q (s) = como ³ + BS ² + CS + D (y, por lo tanto, Q ' (s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="dc702-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="dc702-134">a) Q (0) = V1, so Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="dc702-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="dc702-135">b) Q (1) = V2, so Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="dc702-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="dc702-136">V1 es el contenido de pV1, V2 en el contenido de pV2, T1 es el contenido de pT1 y T2 es el contenido de pT2.</span><span class="sxs-lookup"><span data-stu-id="dc702-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="dc702-137">Estas propiedades se usan para resolver para A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="dc702-137">These properties are used to solve for A, B, C, D.</span></span>

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

<span data-ttu-id="dc702-138">Conecte las soluciones para A, B, C y D para generar Q (s).</span><span class="sxs-lookup"><span data-stu-id="dc702-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="dc702-139">El resultado es:</span><span class="sxs-lookup"><span data-stu-id="dc702-139">This yields:</span></span>

<span data-ttu-id="dc702-140">Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3v2-3V1-2T1-T2) s ² + T1s + v1</span><span class="sxs-lookup"><span data-stu-id="dc702-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="dc702-141">Que se puede reorganizar como:</span><span class="sxs-lookup"><span data-stu-id="dc702-141">Which can be rearranged as:</span></span>

<span data-ttu-id="dc702-142">Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) v2 + (s ³-2s ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="dc702-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="dc702-143">Las curvas spline de Hermite son útiles para controlar la animación, ya que la curva se ejecuta a través de todos los puntos de control.</span><span class="sxs-lookup"><span data-stu-id="dc702-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="dc702-144">Además, dado que la posición y la tangente se especifican explícitamente en los extremos de cada segmento, es fácil crear una curva continua C2 siempre que se asegure de que la posición inicial y la tangente coinciden con los valores finales del último segmento.</span><span class="sxs-lookup"><span data-stu-id="dc702-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="dc702-145">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="dc702-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="dc702-146">De esta manera, la función **D3DXVec3Hermite** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="dc702-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc702-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc702-147">Requirements</span></span>



| <span data-ttu-id="dc702-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc702-148">Requirement</span></span> | <span data-ttu-id="dc702-149">Value</span><span class="sxs-lookup"><span data-stu-id="dc702-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc702-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc702-150">Header</span></span><br/>  | <dl> <span data-ttu-id="dc702-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc702-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dc702-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc702-152">Library</span></span><br/> | <dl> <span data-ttu-id="dc702-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc702-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc702-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc702-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc702-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="dc702-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
