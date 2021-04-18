---
description: Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Función D3DXSHAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b8f65a14cf745e8b378728d4fa6e0a234284d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721453"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="06b29-103">Función D3DXSHAdd (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="06b29-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="06b29-104">Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="06b29-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="06b29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06b29-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="06b29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06b29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b29-107">*pOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06b29-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06b29-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06b29-109">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="06b29-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="06b29-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="06b29-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="06b29-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="06b29-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="06b29-112">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="06b29-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06b29-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06b29-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="06b29-114">Order of the SH evaluation.</span></span> <span data-ttu-id="06b29-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="06b29-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="06b29-116">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="06b29-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="06b29-117">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="06b29-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="06b29-118">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06b29-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="06b29-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06b29-120">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="06b29-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="06b29-121">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06b29-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="06b29-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06b29-123">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="06b29-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b29-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06b29-124">Return value</span></span>

<span data-ttu-id="06b29-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06b29-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06b29-126">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="06b29-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b29-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06b29-127">Remarks</span></span>

<span data-ttu-id="06b29-128">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="06b29-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="06b29-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="06b29-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="06b29-130">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="06b29-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b29-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06b29-131">Requirements</span></span>



| <span data-ttu-id="06b29-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b29-132">Requirement</span></span> | <span data-ttu-id="06b29-133">Value</span><span class="sxs-lookup"><span data-stu-id="06b29-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b29-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06b29-134">Header</span></span><br/>  | <dl> <span data-ttu-id="06b29-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b29-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="06b29-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06b29-136">Library</span></span><br/> | <dl> <span data-ttu-id="06b29-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06b29-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06b29-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="06b29-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b29-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="06b29-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="06b29-140">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06b29-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
