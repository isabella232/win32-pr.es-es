---
description: Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Función D3DXSHAdd (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280457"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="1cc88-103">Función D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="1cc88-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="1cc88-104">Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="1cc88-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc88-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc88-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="1cc88-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cc88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc88-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc88-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc88-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cc88-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cc88-109">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="1cc88-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="1cc88-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="1cc88-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1cc88-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1cc88-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cc88-112">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1cc88-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc88-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cc88-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cc88-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="1cc88-114">Order of the SH evaluation.</span></span> <span data-ttu-id="1cc88-115">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="1cc88-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1cc88-116">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="1cc88-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1cc88-117">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="1cc88-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1cc88-118">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc88-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc88-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cc88-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cc88-120">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="1cc88-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="1cc88-121">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc88-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc88-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cc88-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cc88-123">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="1cc88-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc88-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cc88-124">Return value</span></span>

<span data-ttu-id="1cc88-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cc88-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cc88-126">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="1cc88-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc88-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cc88-127">Remarks</span></span>

<span data-ttu-id="1cc88-128">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="1cc88-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1cc88-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="1cc88-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1cc88-130">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="1cc88-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc88-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc88-131">Requirements</span></span>



| <span data-ttu-id="1cc88-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc88-132">Requirement</span></span> | <span data-ttu-id="1cc88-133">Value</span><span class="sxs-lookup"><span data-stu-id="1cc88-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc88-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc88-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1cc88-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc88-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cc88-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cc88-136">Library</span></span><br/> | <dl> <span data-ttu-id="1cc88-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cc88-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc88-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc88-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc88-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1cc88-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
