---
description: Calcula el producto escalar de dos vectores armónicos (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Función D3DXSHDot (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a69ee929c889232cb29ff1b556dd08ab65a0d6d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424387"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="39629-103">Función D3DXSHDot (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="39629-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="39629-104">Calcula el producto escalar de dos vectores armónicos (SH).</span><span class="sxs-lookup"><span data-stu-id="39629-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="39629-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39629-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="39629-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39629-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="39629-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39629-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39629-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39629-109">Orden de evaluación de armónicos esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="39629-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="39629-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="39629-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="39629-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="39629-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="39629-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="39629-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="39629-113">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39629-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39629-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="39629-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39629-115">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="39629-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="39629-116">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39629-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39629-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="39629-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39629-118">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="39629-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39629-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39629-119">Return value</span></span>

<span data-ttu-id="39629-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39629-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39629-121">Coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="39629-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="39629-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39629-122">Remarks</span></span>

<span data-ttu-id="39629-123">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="39629-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="39629-124">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="39629-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="39629-125">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="39629-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="39629-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39629-126">Requirements</span></span>



| <span data-ttu-id="39629-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="39629-127">Requirement</span></span> | <span data-ttu-id="39629-128">Value</span><span class="sxs-lookup"><span data-stu-id="39629-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39629-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39629-129">Header</span></span><br/>  | <dl> <span data-ttu-id="39629-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="39629-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="39629-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39629-131">Library</span></span><br/> | <dl> <span data-ttu-id="39629-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39629-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39629-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="39629-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39629-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="39629-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="39629-135">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39629-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
