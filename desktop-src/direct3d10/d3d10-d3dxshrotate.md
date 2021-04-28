---
description: 'Función D3DXSHRotate (D3DX10.h): gira el vector de armónico esférico (SH) por la matriz dada.'
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Función D3DXSHRotate (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2f2af3fe59c57ba32bc03bb59233bec72722bbb5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108543"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="4d43d-103">Función D3DXSHRotate (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="4d43d-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="4d43d-104">Gira el vector armónico esférico (SH) por la matriz dada.</span><span class="sxs-lookup"><span data-stu-id="4d43d-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d43d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d43d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="4d43d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d43d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d43d-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4d43d-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d43d-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d43d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4d43d-109">Puntero a coeficientes de salida armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="4d43d-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="4d43d-110">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="4d43d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4d43d-111">Este puntero no debe incluir un alias con pIn.</span><span class="sxs-lookup"><span data-stu-id="4d43d-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="4d43d-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4d43d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4d43d-113">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4d43d-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d43d-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d43d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d43d-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="4d43d-115">Order of the SH evaluation.</span></span> <span data-ttu-id="4d43d-116">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="4d43d-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="4d43d-117">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="4d43d-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4d43d-118">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="4d43d-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="4d43d-119">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4d43d-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d43d-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d43d-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4d43d-121">Puntero a la matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="4d43d-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="4d43d-122">La submatriz de rotación debe ser ortogonal, con una unidad determinante.</span><span class="sxs-lookup"><span data-stu-id="4d43d-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="4d43d-123">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4d43d-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d43d-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d43d-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4d43d-125">Puntero a coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="4d43d-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d43d-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d43d-126">Return value</span></span>

<span data-ttu-id="4d43d-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d43d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4d43d-128">Puntero a coeficientes de salida sh.</span><span class="sxs-lookup"><span data-stu-id="4d43d-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d43d-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d43d-129">Remarks</span></span>

<span data-ttu-id="4d43d-130">Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="4d43d-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="4d43d-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="4d43d-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="4d43d-132">m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="4d43d-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d43d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d43d-133">Requirements</span></span>



| <span data-ttu-id="4d43d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d43d-134">Requirement</span></span> | <span data-ttu-id="4d43d-135">Value</span><span class="sxs-lookup"><span data-stu-id="4d43d-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d43d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d43d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4d43d-137"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="4d43d-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d43d-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d43d-138">Library</span></span><br/> | <dl> <span data-ttu-id="4d43d-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d43d-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d43d-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d43d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d43d-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4d43d-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
