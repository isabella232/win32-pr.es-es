---
description: Gira el vector armónico (SH) de la matriz especificada.
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Función D3DXSHRotate (D3DX10. h)
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
ms.openlocfilehash: 1cdff4a74cb92943db2bd6dc9f207dbac2208afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698357"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="db1ae-103">Función D3DXSHRotate (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="db1ae-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="db1ae-104">Gira el vector armónico (SH) de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="db1ae-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="db1ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db1ae-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="db1ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db1ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1ae-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db1ae-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1ae-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db1ae-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db1ae-109">Puntero a coeficientes de salida de armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="db1ae-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="db1ae-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="db1ae-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="db1ae-111">Este puntero no debe ser un alias con el pIn.</span><span class="sxs-lookup"><span data-stu-id="db1ae-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="db1ae-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="db1ae-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db1ae-113">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="db1ae-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1ae-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db1ae-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db1ae-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="db1ae-115">Order of the SH evaluation.</span></span> <span data-ttu-id="db1ae-116">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="db1ae-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="db1ae-117">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="db1ae-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="db1ae-118">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="db1ae-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="db1ae-119">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db1ae-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1ae-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="db1ae-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db1ae-121">Puntero a la matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="db1ae-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="db1ae-122">La submatriz de rotación debe ser ortogonal, con un determinante de unidad.</span><span class="sxs-lookup"><span data-stu-id="db1ae-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="db1ae-123">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db1ae-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1ae-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="db1ae-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db1ae-125">Puntero a los coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="db1ae-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1ae-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db1ae-126">Return value</span></span>

<span data-ttu-id="db1ae-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db1ae-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db1ae-128">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="db1ae-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="db1ae-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db1ae-129">Remarks</span></span>

<span data-ttu-id="db1ae-130">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="db1ae-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="db1ae-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="db1ae-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="db1ae-132">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="db1ae-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="db1ae-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db1ae-133">Requirements</span></span>



| <span data-ttu-id="db1ae-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="db1ae-134">Requirement</span></span> | <span data-ttu-id="db1ae-135">Value</span><span class="sxs-lookup"><span data-stu-id="db1ae-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db1ae-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db1ae-136">Header</span></span><br/>  | <dl> <span data-ttu-id="db1ae-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="db1ae-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="db1ae-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db1ae-138">Library</span></span><br/> | <dl> <span data-ttu-id="db1ae-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db1ae-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db1ae-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="db1ae-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db1ae-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="db1ae-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
