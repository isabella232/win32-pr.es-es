---
description: 'Función D3DXVec2Hermite (D3DX10Math.h): realiza una interpolación spline de Hermite con los vectores 2D especificados.'
ms.assetid: 2d6ff836-a1a7-4cd0-aea3-4fe344f4e211
title: Función D3DXVec2Hermite (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e64350d4f54fef493ec7fe935474218a1b111503
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108383"
---
# <a name="d3dxvec2hermite-function-d3dx10mathh"></a><span data-ttu-id="d62e3-103">Función D3DXVec2Hermite (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d62e3-103">D3DXVec2Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="d62e3-104">Realiza una interpolación spline de Hermite, utilizando los vectores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="d62e3-104">Performs a Hermite spline interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d62e3-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="d62e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d62e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62e3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d62e3-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d62e3-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d62e3-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62e3-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-112">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="d62e3-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d62e3-113">*pT1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62e3-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-115">Puntero a una estructura D3DXVECTOR2 de origen, un vector tangente.</span><span class="sxs-lookup"><span data-stu-id="d62e3-115">Pointer to a source D3DXVECTOR2 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="d62e3-116">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62e3-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-118">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="d62e3-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d62e3-119">*pT2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62e3-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-121">Puntero a una estructura D3DXVECTOR2 de origen, un vector tangente.</span><span class="sxs-lookup"><span data-stu-id="d62e3-121">Pointer to a source D3DXVECTOR2 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="d62e3-122">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d62e3-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62e3-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d62e3-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d62e3-124">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="d62e3-124">Weighting factor.</span></span> <span data-ttu-id="d62e3-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d62e3-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d62e3-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d62e3-126">Return value</span></span>

<span data-ttu-id="d62e3-127">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d62e3-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d62e3-128">Puntero a una estructura D3DXVECTOR2 que es el resultado de la interpolación spline de Hermite.</span><span class="sxs-lookup"><span data-stu-id="d62e3-128">Pointer to a D3DXVECTOR2 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62e3-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d62e3-129">Remarks</span></span>

<span data-ttu-id="d62e3-130">La **función D3DXVec2Hermite** interpola de (positionA, tangentA) a (positionB, tangentB) mediante la interpolación spline hermite.</span><span class="sxs-lookup"><span data-stu-id="d62e3-130">The **D3DXVec2Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="d62e3-131">La interpolación spline es una generalización de la spline de facilidad de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="d62e3-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="d62e3-132">La rampa es una función de preguntas y respuestas con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d62e3-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="d62e3-133">Q(s) = Aszos + Bs' + Cs + D (y, por lo tanto, Q's) = 3Asmiento + 2B + C)</span><span class="sxs-lookup"><span data-stu-id="d62e3-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="d62e3-134">a) Q(0) = v1, por lo que Q'(0) = t1</span><span class="sxs-lookup"><span data-stu-id="d62e3-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="d62e3-135">b) Q(1) = v2, por lo que Q'(1) = t2</span><span class="sxs-lookup"><span data-stu-id="d62e3-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="d62e3-136">v1 es el contenido de pV1, v2 en el contenido de pV2, t1 es el contenido de pT1 y t2 es el contenido de pT2.</span><span class="sxs-lookup"><span data-stu-id="d62e3-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="d62e3-137">Estas propiedades se usan para resolver A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="d62e3-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="d62e3-138">Conecte las soluciones para A, B, C y D para generar preguntas y respuestas.</span><span class="sxs-lookup"><span data-stu-id="d62e3-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="d62e3-139">El resultado es:</span><span class="sxs-lookup"><span data-stu-id="d62e3-139">This yields:</span></span>

<span data-ttu-id="d62e3-140">Q(s) = (2v1 - 2v2 + t2 + t1)s así + (3v2 - 3v1 - 2t1 - t2)sntes + t1 + v1</span><span class="sxs-lookup"><span data-stu-id="d62e3-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="d62e3-141">Que se puede reorganizar como:</span><span class="sxs-lookup"><span data-stu-id="d62e3-141">Which can be rearranged as:</span></span>

<span data-ttu-id="d62e3-142">Q(s) = (2sntes - 3s además de 1)v1 + (-2sntes + 3s así)v2 + (sntes - 2s además de s)t1 + (sntes - sntes)t2</span><span class="sxs-lookup"><span data-stu-id="d62e3-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="d62e3-143">Las curvas spline de Hermite son útiles para controlar la animación porque la curva se ejecuta a través de todos los puntos de control.</span><span class="sxs-lookup"><span data-stu-id="d62e3-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="d62e3-144">Además, dado que la posición y la tangente se especifican explícitamente en los extremos de cada segmento, es fácil crear una curva continua C2 siempre que se asegúrese de que la posición inicial y la tangente coinciden con los valores finales del último segmento.</span><span class="sxs-lookup"><span data-stu-id="d62e3-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="d62e3-145">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d62e3-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d62e3-146">De este modo, la **función D3DXVec2Hermite** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="d62e3-146">In this way, the **D3DXVec2Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62e3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d62e3-147">Requirements</span></span>



| <span data-ttu-id="d62e3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62e3-148">Requirement</span></span> | <span data-ttu-id="d62e3-149">Value</span><span class="sxs-lookup"><span data-stu-id="d62e3-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d62e3-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d62e3-150">Header</span></span><br/>  | <dl> <span data-ttu-id="d62e3-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d62e3-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d62e3-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d62e3-152">Library</span></span><br/> | <dl> <span data-ttu-id="d62e3-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d62e3-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d62e3-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d62e3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62e3-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d62e3-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
