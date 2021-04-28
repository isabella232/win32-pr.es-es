---
description: 'Función D3DXSHScale (D3dx9math.h): escala un vector de armónica esférica (SH); en otras palabras, pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Función D3DXSHScale (D3dx9math.h)
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
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093863"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="54e0d-103">Función D3DXSHScale (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="54e0d-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="54e0d-104">Escala un vector armónico esférico (SH); en otras palabras, pOut \[ i \] = pA i \[ \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="54e0d-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54e0d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="54e0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e0d-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54e0d-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54e0d-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54e0d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54e0d-109">Puntero a coeficientes de salida de armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="54e0d-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="54e0d-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="54e0d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="54e0d-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="54e0d-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54e0d-112">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54e0d-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54e0d-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54e0d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54e0d-114">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="54e0d-114">Order of the SH evaluation.</span></span> <span data-ttu-id="54e0d-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="54e0d-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="54e0d-116">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="54e0d-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="54e0d-117">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="54e0d-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="54e0d-118">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54e0d-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54e0d-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="54e0d-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54e0d-120">Puntero al vector SH que se escala.</span><span class="sxs-lookup"><span data-stu-id="54e0d-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="54e0d-121">*Escala* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54e0d-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54e0d-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="54e0d-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54e0d-123">Puntero al valor de escala.</span><span class="sxs-lookup"><span data-stu-id="54e0d-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e0d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54e0d-124">Return value</span></span>

<span data-ttu-id="54e0d-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54e0d-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54e0d-126">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="54e0d-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e0d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54e0d-127">Remarks</span></span>

<span data-ttu-id="54e0d-128">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="54e0d-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="54e0d-129">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="54e0d-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="54e0d-130">m es el índice de función base para el valor l especificado y va de -l a l, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="54e0d-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e0d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e0d-131">Requirements</span></span>



| <span data-ttu-id="54e0d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e0d-132">Requirement</span></span> | <span data-ttu-id="54e0d-133">Value</span><span class="sxs-lookup"><span data-stu-id="54e0d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54e0d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54e0d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="54e0d-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="54e0d-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="54e0d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54e0d-136">Library</span></span><br/> | <dl> <span data-ttu-id="54e0d-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="54e0d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54e0d-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54e0d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e0d-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="54e0d-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="54e0d-140">Transferencia de radiancia precalutada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="54e0d-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
