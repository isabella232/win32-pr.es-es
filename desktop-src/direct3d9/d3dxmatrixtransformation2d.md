---
description: 'Función D3DXMatrixTransformation2D (D3dx9math.h): crea una matriz de transformación 2D que representa las transformaciones en el plano xy. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Función D3DXMatrixTransformation2D (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b92a5489569765ef059af9b1023b40fc681b5d0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098123"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="6286b-104">Función D3DXMatrixTransformation2D (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6286b-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="6286b-105">Crea una matriz de transformación 2D que representa las transformaciones en el plano xy.</span><span class="sxs-lookup"><span data-stu-id="6286b-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="6286b-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="6286b-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6286b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6286b-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="6286b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6286b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6286b-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6286b-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6286b-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6286b-111">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que contiene el resultado de las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="6286b-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-112">*pScalingCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-113">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6286b-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6286b-114">Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica el centro de escalado.</span><span class="sxs-lookup"><span data-stu-id="6286b-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="6286b-115">Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6286b-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-116">*pScalingRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6286b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6286b-118">El factor de rotación de escalado.</span><span class="sxs-lookup"><span data-stu-id="6286b-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-119">*pScaling* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-120">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6286b-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6286b-121">Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica la escala.</span><span class="sxs-lookup"><span data-stu-id="6286b-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="6286b-122">Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6286b-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-123">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-124">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6286b-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6286b-125">Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="6286b-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="6286b-126">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6286b-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-127">*Rotación* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-128">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6286b-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6286b-129">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="6286b-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="6286b-130">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6286b-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6286b-131">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6286b-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6286b-132">Puntero a una [**estructura D3DXVECTOR2,**](d3dxvector2.md) que identifica la traducción.</span><span class="sxs-lookup"><span data-stu-id="6286b-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="6286b-133">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6286b-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6286b-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6286b-134">Return value</span></span>

<span data-ttu-id="6286b-135">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6286b-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6286b-136">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que contiene la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="6286b-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6286b-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6286b-137">Remarks</span></span>

<span data-ttu-id="6286b-138">Esta función calcula la matriz de transformación con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="6286b-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="6286b-139">M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/ntes \* \* Ms M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="6286b-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="6286b-140">donde:</span><span class="sxs-lookup"><span data-stu-id="6286b-140">where:</span></span>

<span data-ttu-id="6286b-141">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="6286b-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="6286b-142">M <sub>sc</sub> = matriz del centro de escalado (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="6286b-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="6286b-143">M <sub>sr</sub> = matriz de rotación de escalado (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="6286b-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="6286b-144">Ms = matriz de escalado (*escalado pScaling*)</span><span class="sxs-lookup"><span data-stu-id="6286b-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="6286b-145">M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="6286b-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="6286b-146">M <sub>r</sub> = matriz de rotación (*Rotación*)</span><span class="sxs-lookup"><span data-stu-id="6286b-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="6286b-147">Mt = matriz de traducción (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="6286b-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="6286b-148">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6286b-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6286b-149">De esta manera, la **función D3DXMatrixTransformation2D** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="6286b-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6286b-150">Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="6286b-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6286b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6286b-151">Requirements</span></span>



| <span data-ttu-id="6286b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6286b-152">Requirement</span></span> | <span data-ttu-id="6286b-153">Value</span><span class="sxs-lookup"><span data-stu-id="6286b-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6286b-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6286b-154">Header</span></span><br/>  | <dl> <span data-ttu-id="6286b-155"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6286b-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6286b-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6286b-156">Library</span></span><br/> | <dl> <span data-ttu-id="6286b-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6286b-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6286b-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6286b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6286b-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6286b-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6286b-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="6286b-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="6286b-161">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6286b-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
