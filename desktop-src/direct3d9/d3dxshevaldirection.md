---
description: 'Función D3DXSHEvalDirection (D3dx9math.h): evalúa las funciones básicas de armónica esférica (SH) a partir de un vector de dirección de entrada.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Función D3DXSHEvalDirection (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093970"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="74a85-103">Función D3DXSHEvalDirection (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="74a85-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="74a85-104">Evalúa las funciones básicas de armónica esférica (SH) a partir de un vector de dirección de entrada.</span><span class="sxs-lookup"><span data-stu-id="74a85-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a85-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74a85-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="74a85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74a85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a85-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74a85-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74a85-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="74a85-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="74a85-109">Puntero a coeficientes de salida de armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="74a85-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="74a85-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="74a85-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="74a85-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="74a85-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="74a85-112">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="74a85-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a85-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74a85-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74a85-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="74a85-114">Order of the SH evaluation.</span></span> <span data-ttu-id="74a85-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="74a85-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="74a85-116">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="74a85-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="74a85-117">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="74a85-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="74a85-118">*pDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="74a85-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a85-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="74a85-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="74a85-120">(x, y, z) vector de dirección en el que se evaluarán las funciones de base sh.</span><span class="sxs-lookup"><span data-stu-id="74a85-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="74a85-121">Debe normalizarse.</span><span class="sxs-lookup"><span data-stu-id="74a85-121">Must be normalized.</span></span> <span data-ttu-id="74a85-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="74a85-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a85-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74a85-123">Return value</span></span>

<span data-ttu-id="74a85-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="74a85-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="74a85-125">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="74a85-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="74a85-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="74a85-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="74a85-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74a85-127">Remarks</span></span>

<span data-ttu-id="74a85-128">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="74a85-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="74a85-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="74a85-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="74a85-130">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="74a85-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="74a85-131">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección [](coordinate-systems.md)se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.</span><span class="sxs-lookup"><span data-stu-id="74a85-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="74a85-133">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="74a85-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="74a85-134">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="74a85-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="74a85-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74a85-136">Requirements</span></span>



| <span data-ttu-id="74a85-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a85-137">Requirement</span></span> | <span data-ttu-id="74a85-138">Value</span><span class="sxs-lookup"><span data-stu-id="74a85-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74a85-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74a85-139">Header</span></span><br/>  | <dl> <span data-ttu-id="74a85-140"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="74a85-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="74a85-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74a85-141">Library</span></span><br/> | <dl> <span data-ttu-id="74a85-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="74a85-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74a85-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74a85-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a85-144">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="74a85-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="74a85-145">Transferencia de radiancia precalutada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="74a85-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
