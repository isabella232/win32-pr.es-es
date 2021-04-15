---
description: Calcula el producto escalar de dos vectores armónicos (SH).
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Función D3DXSHDot (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708000"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="2d48c-103">Función D3DXSHDot (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2d48c-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="2d48c-104">Calcula el producto escalar de dos vectores armónicos (SH).</span><span class="sxs-lookup"><span data-stu-id="2d48c-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d48c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d48c-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="2d48c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d48c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d48c-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2d48c-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d48c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d48c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d48c-109">Orden de evaluación de armónicos esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="2d48c-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="2d48c-110">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2d48c-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2d48c-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="2d48c-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2d48c-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="2d48c-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2d48c-113">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d48c-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d48c-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d48c-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d48c-115">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="2d48c-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="2d48c-116">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d48c-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d48c-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d48c-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d48c-118">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="2d48c-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d48c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d48c-119">Return value</span></span>

<span data-ttu-id="2d48c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d48c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d48c-121">Coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="2d48c-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d48c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d48c-122">Remarks</span></span>

<span data-ttu-id="2d48c-123">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="2d48c-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2d48c-124">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="2d48c-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2d48c-125">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2d48c-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d48c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d48c-126">Requirements</span></span>



| <span data-ttu-id="2d48c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d48c-127">Requirement</span></span> | <span data-ttu-id="2d48c-128">Value</span><span class="sxs-lookup"><span data-stu-id="2d48c-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d48c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d48c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2d48c-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d48c-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d48c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d48c-131">Library</span></span><br/> | <dl> <span data-ttu-id="2d48c-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d48c-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d48c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d48c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d48c-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2d48c-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
