---
description: 'Función D3DXSHRotateZ (D3DX10.h): gira el vector de armónico esférico (SH) en el eje Z según el ángulo especificado.'
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Función D3DXSHRotateZ (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55e4663057bd25ac9768a5913963a5511b662f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108533"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="e42b5-103">Función D3DXSHRotateZ (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="e42b5-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="e42b5-104">Gira el vector armónico esférico (SH) en el eje z mediante el ángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="e42b5-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e42b5-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="e42b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e42b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42b5-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e42b5-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42b5-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e42b5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e42b5-109">Puntero a coeficientes de salida de armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="e42b5-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="e42b5-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="e42b5-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e42b5-111">Este puntero no debe incluir un alias con pIn.</span><span class="sxs-lookup"><span data-stu-id="e42b5-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="e42b5-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e42b5-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e42b5-113">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e42b5-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42b5-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e42b5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e42b5-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="e42b5-115">Order of the SH evaluation.</span></span> <span data-ttu-id="e42b5-116">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="e42b5-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e42b5-117">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="e42b5-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e42b5-118">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="e42b5-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e42b5-119">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e42b5-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42b5-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e42b5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e42b5-121">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="e42b5-121">Rotation angle in radians.</span></span> <span data-ttu-id="e42b5-122">La rotación se realiza alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="e42b5-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e42b5-123">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e42b5-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42b5-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e42b5-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e42b5-125">Puntero a coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="e42b5-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42b5-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e42b5-126">Return value</span></span>

<span data-ttu-id="e42b5-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e42b5-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e42b5-128">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="e42b5-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="e42b5-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e42b5-129">Remarks</span></span>

<span data-ttu-id="e42b5-130">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="e42b5-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e42b5-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="e42b5-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e42b5-132">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="e42b5-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e42b5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e42b5-133">Requirements</span></span>



| <span data-ttu-id="e42b5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e42b5-134">Requirement</span></span> | <span data-ttu-id="e42b5-135">Value</span><span class="sxs-lookup"><span data-stu-id="e42b5-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e42b5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e42b5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e42b5-137"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="e42b5-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e42b5-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e42b5-138">Library</span></span><br/> | <dl> <span data-ttu-id="e42b5-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e42b5-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e42b5-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e42b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42b5-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e42b5-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
