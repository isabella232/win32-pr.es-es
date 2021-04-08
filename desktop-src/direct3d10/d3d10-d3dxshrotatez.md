---
description: Gira el vector armónico (SH) del eje z en el ángulo especificado.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Función D3DXSHRotateZ (D3DX10. h)
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
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003892"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="6ac50-103">Función D3DXSHRotateZ (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6ac50-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="6ac50-104">Gira el vector armónico (SH) del eje z en el ángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="6ac50-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac50-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ac50-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="6ac50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ac50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac50-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac50-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac50-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ac50-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6ac50-109">Puntero a coeficientes de salida de armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="6ac50-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="6ac50-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="6ac50-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6ac50-111">Este puntero no debe ser un alias con el pIn.</span><span class="sxs-lookup"><span data-stu-id="6ac50-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="6ac50-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6ac50-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6ac50-113">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6ac50-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac50-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac50-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac50-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="6ac50-115">Order of the SH evaluation.</span></span> <span data-ttu-id="6ac50-116">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="6ac50-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6ac50-117">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="6ac50-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6ac50-118">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="6ac50-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6ac50-119">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac50-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac50-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac50-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac50-121">Ángulo de giro en radianes.</span><span class="sxs-lookup"><span data-stu-id="6ac50-121">Rotation angle in radians.</span></span> <span data-ttu-id="6ac50-122">La rotación se realiza alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="6ac50-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6ac50-123">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac50-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac50-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac50-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6ac50-125">Puntero a los coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="6ac50-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac50-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ac50-126">Return value</span></span>

<span data-ttu-id="6ac50-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ac50-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6ac50-128">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="6ac50-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac50-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ac50-129">Remarks</span></span>

<span data-ttu-id="6ac50-130">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="6ac50-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="6ac50-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="6ac50-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="6ac50-132">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="6ac50-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac50-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ac50-133">Requirements</span></span>



| <span data-ttu-id="6ac50-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac50-134">Requirement</span></span> | <span data-ttu-id="6ac50-135">Value</span><span class="sxs-lookup"><span data-stu-id="6ac50-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac50-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ac50-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac50-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac50-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ac50-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ac50-138">Library</span></span><br/> | <dl> <span data-ttu-id="6ac50-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ac50-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac50-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ac50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac50-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6ac50-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
