---
description: Escala un vector armónico (SH) esférico; en otras palabras, pOut \[ i \] = PA \[ i \] \* Scale.
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Función D3DXSHScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1a8cc7c63880876f85969443502db3d5fb3278c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157172"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="9e0fb-103">Función D3DXSHScale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9e0fb-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="9e0fb-104">Escala un vector armónico (SH) esférico; en otras palabras, pOut \[ i \] = PA \[ i \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e0fb-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="9e0fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e0fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e0fb-107">*pOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0fb-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e0fb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9e0fb-109">Puntero a coeficientes de salida de armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="9e0fb-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="9e0fb-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="9e0fb-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9e0fb-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fb-112">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0fb-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e0fb-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e0fb-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-114">Order of the SH evaluation.</span></span> <span data-ttu-id="9e0fb-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9e0fb-116">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="9e0fb-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="9e0fb-117">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fb-118">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0fb-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e0fb-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9e0fb-120">Puntero al vector SH que se va a escalar.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fb-121">*Escala* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0fb-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e0fb-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9e0fb-123">Puntero al valor de escala.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e0fb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e0fb-124">Return value</span></span>

<span data-ttu-id="9e0fb-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e0fb-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9e0fb-126">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e0fb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e0fb-127">Remarks</span></span>

<span data-ttu-id="9e0fb-128">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="9e0fb-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="9e0fb-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="9e0fb-130">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0fb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e0fb-131">Requirements</span></span>



| <span data-ttu-id="9e0fb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0fb-132">Requirement</span></span> | <span data-ttu-id="9e0fb-133">Value</span><span class="sxs-lookup"><span data-stu-id="9e0fb-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0fb-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e0fb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9e0fb-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0fb-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9e0fb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e0fb-136">Library</span></span><br/> | <dl> <span data-ttu-id="9e0fb-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e0fb-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e0fb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e0fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0fb-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="9e0fb-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9e0fb-140">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9e0fb-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
