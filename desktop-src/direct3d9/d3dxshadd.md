---
description: 'Función D3DXSHAdd (D3dx9math.h): agrega dos vectores de armónica esférica (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Función D3DXSHAdd (D3dx9math.h)
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
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117963"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="23dfc-103">Función D3DXSHAdd (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="23dfc-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="23dfc-104">Agrega dos vectores armónicos esféricos (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="23dfc-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="23dfc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23dfc-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="23dfc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23dfc-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23dfc-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23dfc-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23dfc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23dfc-109">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="23dfc-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="23dfc-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="23dfc-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="23dfc-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="23dfc-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="23dfc-112">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="23dfc-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23dfc-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23dfc-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23dfc-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="23dfc-114">Order of the SH evaluation.</span></span> <span data-ttu-id="23dfc-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="23dfc-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="23dfc-116">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="23dfc-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="23dfc-117">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="23dfc-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="23dfc-118">*pA* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="23dfc-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23dfc-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="23dfc-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23dfc-120">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="23dfc-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="23dfc-121">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="23dfc-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23dfc-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="23dfc-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23dfc-123">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="23dfc-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23dfc-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23dfc-124">Return value</span></span>

<span data-ttu-id="23dfc-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23dfc-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23dfc-126">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="23dfc-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="23dfc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23dfc-127">Remarks</span></span>

<span data-ttu-id="23dfc-128">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="23dfc-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="23dfc-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="23dfc-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="23dfc-130">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="23dfc-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="23dfc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23dfc-131">Requirements</span></span>



| <span data-ttu-id="23dfc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="23dfc-132">Requirement</span></span> | <span data-ttu-id="23dfc-133">Value</span><span class="sxs-lookup"><span data-stu-id="23dfc-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23dfc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23dfc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="23dfc-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="23dfc-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="23dfc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23dfc-136">Library</span></span><br/> | <dl> <span data-ttu-id="23dfc-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="23dfc-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23dfc-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="23dfc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23dfc-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="23dfc-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="23dfc-140">Transferencia de radiancia precalcalada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23dfc-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
