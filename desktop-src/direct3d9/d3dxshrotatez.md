---
description: Gira el vector armónico (SH) del eje z en el ángulo especificado.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Función D3DXSHRotateZ (D3dx9math. h)
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
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424384"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="3053c-103">Función D3DXSHRotateZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3053c-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="3053c-104">Gira el vector armónico (SH) del eje z en el ángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="3053c-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3053c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3053c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="3053c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3053c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3053c-107">*pOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3053c-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3053c-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3053c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3053c-109">Puntero a coeficientes de salida de armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="3053c-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="3053c-110">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="3053c-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3053c-111">Este puntero no debe ser un alias con el *pIn*.</span><span class="sxs-lookup"><span data-stu-id="3053c-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="3053c-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3053c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3053c-113">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3053c-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3053c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3053c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3053c-115">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="3053c-115">Order of the SH evaluation.</span></span> <span data-ttu-id="3053c-116">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="3053c-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3053c-117">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="3053c-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3053c-118">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="3053c-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3053c-119">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3053c-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3053c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3053c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3053c-121">Ángulo de giro en radianes.</span><span class="sxs-lookup"><span data-stu-id="3053c-121">Rotation angle in radians.</span></span> <span data-ttu-id="3053c-122">La rotación se realiza alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="3053c-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="3053c-123">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3053c-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3053c-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3053c-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3053c-125">Puntero a los coeficientes SH girados.</span><span class="sxs-lookup"><span data-stu-id="3053c-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3053c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3053c-126">Return value</span></span>

<span data-ttu-id="3053c-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3053c-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3053c-128">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="3053c-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="3053c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3053c-129">Remarks</span></span>

<span data-ttu-id="3053c-130">Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:</span><span class="sxs-lookup"><span data-stu-id="3053c-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="3053c-131">l es el grado de la función base.</span><span class="sxs-lookup"><span data-stu-id="3053c-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="3053c-132">m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="3053c-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="3053c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3053c-133">Requirements</span></span>



| <span data-ttu-id="3053c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3053c-134">Requirement</span></span> | <span data-ttu-id="3053c-135">Value</span><span class="sxs-lookup"><span data-stu-id="3053c-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3053c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3053c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3053c-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3053c-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3053c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3053c-138">Library</span></span><br/> | <dl> <span data-ttu-id="3053c-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3053c-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3053c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3053c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3053c-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3053c-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3053c-142">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3053c-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
