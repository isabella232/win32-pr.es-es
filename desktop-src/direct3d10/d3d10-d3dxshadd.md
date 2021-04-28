---
description: 'Función D3DXSHAdd (D3DX10.h): agrega dos vectores de armónica esférica (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Función D3DXSHAdd (D3DX10.h)
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
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108663"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="2bdf5-103">Función D3DXSHAdd (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2bdf5-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="2bdf5-104">Agrega dos vectores armónicos esféricos (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="2bdf5-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdf5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bdf5-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="2bdf5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bdf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bdf5-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2bdf5-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdf5-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bdf5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bdf5-109">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="2bdf5-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bdf5-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2bdf5-112">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2bdf5-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdf5-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bdf5-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bdf5-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-114">Order of the SH evaluation.</span></span> <span data-ttu-id="2bdf5-115">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2bdf5-116">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2bdf5-117">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2bdf5-118">*pA* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2bdf5-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdf5-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bdf5-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bdf5-120">Puntero al primer vector SH.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="2bdf5-121">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2bdf5-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdf5-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2bdf5-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bdf5-123">Puntero al segundo vector SH.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bdf5-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bdf5-124">Return value</span></span>

<span data-ttu-id="2bdf5-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bdf5-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2bdf5-126">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdf5-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bdf5-127">Remarks</span></span>

<span data-ttu-id="2bdf5-128">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="2bdf5-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2bdf5-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2bdf5-130">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2bdf5-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdf5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bdf5-131">Requirements</span></span>



| <span data-ttu-id="2bdf5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bdf5-132">Requirement</span></span> | <span data-ttu-id="2bdf5-133">Value</span><span class="sxs-lookup"><span data-stu-id="2bdf5-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdf5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bdf5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2bdf5-135"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2bdf5-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bdf5-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bdf5-136">Library</span></span><br/> | <dl> <span data-ttu-id="2bdf5-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bdf5-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bdf5-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2bdf5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdf5-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2bdf5-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
