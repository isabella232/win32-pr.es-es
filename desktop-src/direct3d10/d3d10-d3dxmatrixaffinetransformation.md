---
description: 'Función D3DXMatrixAffineTransformation (D3DX10Math.h): crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Función D3DXMatrixAffineTransformation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113183"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="4da1f-104">Función D3DXMatrixAffineTransformation (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4da1f-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="4da1f-105">Crea una matriz de transformación afín 3D.</span><span class="sxs-lookup"><span data-stu-id="4da1f-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="4da1f-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="4da1f-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da1f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4da1f-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="4da1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4da1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da1f-109">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4da1f-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1f-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4da1f-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4da1f-111">Puntero a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4da1f-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4da1f-112">*Escalado* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4da1f-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1f-113">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4da1f-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4da1f-114">Factor de escalado.</span><span class="sxs-lookup"><span data-stu-id="4da1f-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="4da1f-115">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4da1f-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1f-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4da1f-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4da1f-117">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="4da1f-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="4da1f-118">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4da1f-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4da1f-119">*pRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4da1f-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1f-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4da1f-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4da1f-121">Puntero a [**un D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="4da1f-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="4da1f-122">Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4da1f-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4da1f-123">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4da1f-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1f-124">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4da1f-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4da1f-125">Puntero a una estructura D3DXVECTOR3 que representa la traducción.</span><span class="sxs-lookup"><span data-stu-id="4da1f-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="4da1f-126">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4da1f-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da1f-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4da1f-127">Return value</span></span>

<span data-ttu-id="4da1f-128">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4da1f-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4da1f-129">Puntero a una estructura D3DXMATRIX que es una matriz de transformación afín.</span><span class="sxs-lookup"><span data-stu-id="4da1f-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da1f-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4da1f-130">Remarks</span></span>

<span data-ttu-id="4da1f-131">Esta función calcula la matriz de transformación afín con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="4da1f-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="4da1f-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="4da1f-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="4da1f-133">donde:</span><span class="sxs-lookup"><span data-stu-id="4da1f-133">where:</span></span>

<span data-ttu-id="4da1f-134">M<sub>out</sub> = matriz de salida (pOut)</span><span class="sxs-lookup"><span data-stu-id="4da1f-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="4da1f-135">Ms = matriz de escalado (escalado)</span><span class="sxs-lookup"><span data-stu-id="4da1f-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="4da1f-136">M<sub>rc</sub> = centro de la matriz de rotación (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="4da1f-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="4da1f-137">M<sub>r</sub> = matriz de rotación (pRotation)</span><span class="sxs-lookup"><span data-stu-id="4da1f-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="4da1f-138">Mt = matriz de traducción (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="4da1f-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="4da1f-139">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="4da1f-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4da1f-140">De este modo, la función D3DXMatrixAffineTransformation se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="4da1f-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4da1f-141">Para las transformaciones de afín 2D, use D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="4da1f-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da1f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da1f-142">Requirements</span></span>



| <span data-ttu-id="4da1f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da1f-143">Requirement</span></span> | <span data-ttu-id="4da1f-144">Value</span><span class="sxs-lookup"><span data-stu-id="4da1f-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4da1f-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4da1f-145">Header</span></span><br/>  | <dl> <span data-ttu-id="4da1f-146"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4da1f-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4da1f-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4da1f-147">Library</span></span><br/> | <dl> <span data-ttu-id="4da1f-148"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4da1f-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4da1f-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4da1f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da1f-150">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4da1f-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
