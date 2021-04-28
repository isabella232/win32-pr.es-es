---
description: 'Función D3DXSHRotateZ (D3dx9math.h): gira el vector de armónico esférico (SH) en el eje Z por el ángulo especificado.'
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Función D3DXSHRotateZ (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117853"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="dc145-103">Función D3DXSHRotateZ (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="dc145-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="dc145-104">Gira el vector armónico esférico (SH) en el eje Z por el ángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="dc145-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc145-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc145-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="dc145-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc145-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc145-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc145-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc145-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc145-109">Puntero a coeficientes de salida armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="dc145-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="dc145-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="dc145-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="dc145-111">Este puntero no debe incluir un alias *con pIn*.</span><span class="sxs-lookup"><span data-stu-id="dc145-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="dc145-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="dc145-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dc145-113">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dc145-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc145-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc145-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc145-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="dc145-115">Order of the SH evaluation.</span></span> <span data-ttu-id="dc145-116">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="dc145-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="dc145-117">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="dc145-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="dc145-118">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="dc145-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="dc145-119">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dc145-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc145-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc145-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc145-121">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="dc145-121">Rotation angle in radians.</span></span> <span data-ttu-id="dc145-122">La rotación se realiza alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="dc145-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="dc145-123">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dc145-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc145-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc145-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc145-125">Puntero a coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="dc145-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc145-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc145-126">Return value</span></span>

<span data-ttu-id="dc145-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc145-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc145-128">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="dc145-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc145-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc145-129">Remarks</span></span>

<span data-ttu-id="dc145-130">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="dc145-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="dc145-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="dc145-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="dc145-132">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="dc145-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc145-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc145-133">Requirements</span></span>



| <span data-ttu-id="dc145-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc145-134">Requirement</span></span> | <span data-ttu-id="dc145-135">Value</span><span class="sxs-lookup"><span data-stu-id="dc145-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc145-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc145-136">Header</span></span><br/>  | <dl> <span data-ttu-id="dc145-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc145-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dc145-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc145-138">Library</span></span><br/> | <dl> <span data-ttu-id="dc145-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc145-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc145-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc145-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc145-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="dc145-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="dc145-142">Transferencia de radiancia precalcalada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc145-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
