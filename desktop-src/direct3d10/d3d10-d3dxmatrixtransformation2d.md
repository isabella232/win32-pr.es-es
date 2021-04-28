---
description: 'Función D3DXMatrixTransformation2D (D3DX10Math.h): crea una matriz de transformación 2D que representa las transformaciones en el plano xy. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Función D3DXMatrixTransformation2D (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ef112c346fd222f5e25935740e47ab62273628f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103363"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a><span data-ttu-id="7e145-104">Función D3DXMatrixTransformation2D (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7e145-104">D3DXMatrixTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="7e145-105">Crea una matriz de transformación 2D que representa las transformaciones en el plano xy.</span><span class="sxs-lookup"><span data-stu-id="7e145-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="7e145-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="7e145-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e145-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e145-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="7e145-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e145-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7e145-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e145-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7e145-111">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que contiene el resultado de las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7e145-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-112">*pScalingCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-113">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e145-113">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e145-114">Puntero a [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)un punto que identifica el centro de escalado.</span><span class="sxs-lookup"><span data-stu-id="7e145-114">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the scaling center.</span></span> <span data-ttu-id="7e145-115">Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7e145-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-116">*ScalingRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-116">*ScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e145-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e145-118">Puntero al factor de rotación de escalado.</span><span class="sxs-lookup"><span data-stu-id="7e145-118">Pointer to the scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-119">*pScaling* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e145-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e145-121">Puntero a una estructura D3DXVECTOR2, un punto que identifica la escala.</span><span class="sxs-lookup"><span data-stu-id="7e145-121">Pointer to a D3DXVECTOR2 structure, a point identifying the scale.</span></span> <span data-ttu-id="7e145-122">Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7e145-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-123">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-124">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e145-124">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e145-125">Puntero a una estructura D3DXVECTOR2, un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="7e145-125">Pointer to a D3DXVECTOR2 structure, a point identifying the rotation center.</span></span> <span data-ttu-id="7e145-126">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7e145-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-127">*Rotación* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-128">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e145-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e145-129">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="7e145-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="7e145-130">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7e145-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e145-131">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e145-131">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e145-132">Puntero a una estructura D3DXVECTOR2, que identifica la traducción.</span><span class="sxs-lookup"><span data-stu-id="7e145-132">Pointer to a D3DXVECTOR2 structure, identifying the translation.</span></span> <span data-ttu-id="7e145-133">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7e145-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e145-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e145-134">Return value</span></span>

<span data-ttu-id="7e145-135">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e145-135">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7e145-136">Puntero a una estructura D3DXMATRIX que contiene la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="7e145-136">Pointer to a D3DXMATRIX structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e145-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e145-137">Remarks</span></span>

<span data-ttu-id="7e145-138">Esta función calcula la matriz de transformación con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="7e145-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="7e145-139">M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/ntes \* \* Ms M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="7e145-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="7e145-140">donde:</span><span class="sxs-lookup"><span data-stu-id="7e145-140">where:</span></span>

<span data-ttu-id="7e145-141">M<sub>out</sub> = matriz de salida (pOut)</span><span class="sxs-lookup"><span data-stu-id="7e145-141">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="7e145-142">M<sub>sc</sub> = matriz del centro de escalado (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="7e145-142">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="7e145-143">M<sub>sr</sub> = matriz de rotación de escalado (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="7e145-143">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="7e145-144">Ms = matriz de escalado (escalado pScaling)</span><span class="sxs-lookup"><span data-stu-id="7e145-144">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="7e145-145">M<sub>rc</sub> = centro de la matriz de rotación (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="7e145-145">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="7e145-146">M<sub>r</sub> = matriz de rotación (rotación)</span><span class="sxs-lookup"><span data-stu-id="7e145-146">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="7e145-147">Mt = matriz de traducción (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="7e145-147">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="7e145-148">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="7e145-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7e145-149">De esta manera, la función D3DXMatrixTransformation2D se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="7e145-149">In this way, the D3DXMatrixTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7e145-150">Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="7e145-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e145-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e145-151">Requirements</span></span>



| <span data-ttu-id="7e145-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e145-152">Requirement</span></span> | <span data-ttu-id="7e145-153">Value</span><span class="sxs-lookup"><span data-stu-id="7e145-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e145-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e145-154">Header</span></span><br/>  | <dl> <span data-ttu-id="7e145-155"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7e145-155"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7e145-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e145-156">Library</span></span><br/> | <dl> <span data-ttu-id="7e145-157"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e145-157"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e145-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e145-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e145-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7e145-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
