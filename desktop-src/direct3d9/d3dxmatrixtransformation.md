---
description: 'Función D3DXMatrixTransformation (D3dx9math.h): crea una matriz de transformación. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Función D3DXMatrixTransformation (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098133"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="0cbcf-104">Función D3DXMatrixTransformation (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="0cbcf-105">Crea una matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-105">Builds a transformation matrix.</span></span> <span data-ttu-id="0cbcf-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbcf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cbcf-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="0cbcf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cbcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cbcf-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0cbcf-111">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-112">*pScalingCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cbcf-114">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que identifica el punto central de escalado.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="0cbcf-115">Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-116">*pScalingRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0cbcf-118">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación de escalado.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="0cbcf-119">Si este argumento es **NULL,** se aplica una matriz M <sub>sr</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-120">*pScaling* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cbcf-122">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) el vector de escalado.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="0cbcf-123">Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-124">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-125">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cbcf-126">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="0cbcf-127">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-128">*pRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-129">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0cbcf-130">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="0cbcf-131">Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0cbcf-132">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0cbcf-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbcf-133">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cbcf-134">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que representa la traducción.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="0cbcf-135">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cbcf-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cbcf-136">Return value</span></span>

<span data-ttu-id="0cbcf-137">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cbcf-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0cbcf-138">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbcf-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cbcf-139">Remarks</span></span>

<span data-ttu-id="0cbcf-140">Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="0cbcf-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="0cbcf-141">M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/¹ \* Ms M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="0cbcf-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="0cbcf-142">donde:</span><span class="sxs-lookup"><span data-stu-id="0cbcf-142">where:</span></span>

<span data-ttu-id="0cbcf-143">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="0cbcf-144">M <sub>sc</sub> = matriz del centro de escalado (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="0cbcf-145">M <sub>sr</sub> = matriz de rotación de escalado (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="0cbcf-146">Ms = matriz de escalado (*escalado pScaling*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="0cbcf-147">M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="0cbcf-148">M <sub>r</sub> = matriz de rotación (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="0cbcf-149">Mt = matriz de traducción (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="0cbcf-150">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="0cbcf-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0cbcf-151">De este modo, la **función D3DXMatrixTransformation** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="0cbcf-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0cbcf-152">Para las transformaciones 2D, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="0cbcf-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbcf-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cbcf-153">Requirements</span></span>



| <span data-ttu-id="0cbcf-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cbcf-154">Requirement</span></span> | <span data-ttu-id="0cbcf-155">Value</span><span class="sxs-lookup"><span data-stu-id="0cbcf-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbcf-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cbcf-156">Header</span></span><br/>  | <dl> <span data-ttu-id="0cbcf-157"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cbcf-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0cbcf-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cbcf-158">Library</span></span><br/> | <dl> <span data-ttu-id="0cbcf-159"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cbcf-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cbcf-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0cbcf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbcf-161">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0cbcf-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0cbcf-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="0cbcf-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="0cbcf-163">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cbcf-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




