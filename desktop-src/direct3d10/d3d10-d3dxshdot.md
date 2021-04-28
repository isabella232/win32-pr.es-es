---
description: 'Función D3DXSHDot (D3DX10.h): calcula el producto de puntos de dos vectores de armónica esférica (SH).'
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Función D3DXSHDot (D3DX10.h)
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
ms.openlocfilehash: 3ea3e839ff7a5fc038cf40a6402db4a358da8b39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108633"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="8c879-103">Función D3DXSHDot (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="8c879-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="8c879-104">Calcula el producto de punto de dos vectores armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="8c879-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c879-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c879-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="8c879-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c879-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c879-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8c879-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c879-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c879-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c879-109">Orden de la evaluación del armónico esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="8c879-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="8c879-110">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="8c879-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="8c879-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="8c879-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8c879-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="8c879-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="8c879-113">*pA* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8c879-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c879-114">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c879-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8c879-115">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="8c879-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="8c879-116">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8c879-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c879-117">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c879-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8c879-118">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="8c879-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c879-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c879-119">Return value</span></span>

<span data-ttu-id="8c879-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c879-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c879-121">Coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="8c879-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c879-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c879-122">Remarks</span></span>

<span data-ttu-id="8c879-123">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="8c879-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="8c879-124">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="8c879-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="8c879-125">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="8c879-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c879-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c879-126">Requirements</span></span>



| <span data-ttu-id="8c879-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c879-127">Requirement</span></span> | <span data-ttu-id="8c879-128">Value</span><span class="sxs-lookup"><span data-stu-id="8c879-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c879-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c879-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8c879-130"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c879-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c879-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c879-131">Library</span></span><br/> | <dl> <span data-ttu-id="8c879-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c879-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c879-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c879-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c879-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8c879-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
