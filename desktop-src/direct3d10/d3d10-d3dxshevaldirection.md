---
description: Evalúa las funciones de base de armónicos esféricos (SH) a partir de un vector de dirección de entrada.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Función D3DXSHEvalDirection (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 698873f3278b37970120b03c25918096762ead34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104552750"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="a1b7a-103">Función D3DXSHEvalDirection (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="a1b7a-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="a1b7a-104">Evalúa las funciones de base de armónicos esféricos (SH) a partir de un vector de dirección de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1b7a-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="a1b7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1b7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b7a-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1b7a-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b7a-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1b7a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1b7a-109">Puntero a coeficientes de salida de armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="a1b7a-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="a1b7a-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="a1b7a-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a1b7a-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a1b7a-112">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a1b7a-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b7a-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1b7a-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1b7a-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-114">Order of the SH evaluation.</span></span> <span data-ttu-id="a1b7a-115">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a1b7a-116">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="a1b7a-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a1b7a-117">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a1b7a-118">*pDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1b7a-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b7a-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1b7a-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1b7a-120">(x, y, z): Vector de dirección en el que se van a evaluar las funciones de base de SH.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="a1b7a-121">Debe normalizarse.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-121">Must be normalized.</span></span> <span data-ttu-id="a1b7a-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b7a-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1b7a-123">Return value</span></span>

<span data-ttu-id="a1b7a-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1b7a-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1b7a-125">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="a1b7a-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1b7a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1b7a-127">Remarks</span></span>

<span data-ttu-id="a1b7a-128">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="a1b7a-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="a1b7a-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="a1b7a-130">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="a1b7a-131">En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la mano derecha y la PHI, el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="a1b7a-133">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="a1b7a-134">El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="a1b7a-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="a1b7a-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1b7a-136">Requirements</span></span>



| <span data-ttu-id="a1b7a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b7a-137">Requirement</span></span> | <span data-ttu-id="a1b7a-138">Value</span><span class="sxs-lookup"><span data-stu-id="a1b7a-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b7a-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1b7a-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a1b7a-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b7a-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1b7a-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1b7a-141">Library</span></span><br/> | <dl> <span data-ttu-id="a1b7a-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1b7a-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b7a-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1b7a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b7a-144">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a1b7a-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
