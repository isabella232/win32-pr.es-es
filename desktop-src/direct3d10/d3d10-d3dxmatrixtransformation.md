---
description: 'Función D3DXMatrixTransformation (D3DX10Math.h): crea una matriz de transformación. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Función D3DXMatrixTransformation (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 10ed63b292dd69acb58d8567e6336b5aab4f7997
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108903"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a><span data-ttu-id="ad4ce-104">Función D3DXMatrixTransformation (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-104">D3DXMatrixTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="ad4ce-105">Crea una matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-105">Builds a transformation matrix.</span></span> <span data-ttu-id="ad4ce-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad4ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad4ce-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ad4ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad4ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad4ce-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad4ce-111">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-112">*pScalingCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-113">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-113">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad4ce-114">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que identifica el punto central de escalado.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-114">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the scaling center point.</span></span> <span data-ttu-id="ad4ce-115">Si este argumento es **NULL,** se aplica una matriz <sub>M sc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-116">*pScalingRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ad4ce-118">Puntero a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación de escalado.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the scaling rotation.</span></span> <span data-ttu-id="ad4ce-119">Si este argumento es **NULL,** se aplica una matriz M <sub>sr</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-120">*pScaling* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-121">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-121">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad4ce-122">Puntero a una estructura D3DXVECTOR3, el vector de escalado.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-122">Pointer to a D3DXVECTOR3 structure, the scaling vector.</span></span> <span data-ttu-id="ad4ce-123">Si este argumento es **NULL,** se aplica una matriz Ms de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-124">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-125">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-125">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad4ce-126">Puntero a una estructura D3DXVECTOR3, un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-126">Pointer to a D3DXVECTOR3 structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="ad4ce-127">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-128">*pRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-129">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-129">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ad4ce-130">Puntero a una estructura D3DXQUATERNION que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-130">Pointer to a D3DXQUATERNION structure that specifies the rotation.</span></span> <span data-ttu-id="ad4ce-131">Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ce-132">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ad4ce-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ce-133">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-133">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad4ce-134">Puntero a una estructura D3DXVECTOR3, que representa la traducción.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-134">Pointer to a D3DXVECTOR3 structure, representing the translation.</span></span> <span data-ttu-id="ad4ce-135">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad4ce-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad4ce-136">Return value</span></span>

<span data-ttu-id="ad4ce-137">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad4ce-137">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad4ce-138">Puntero a una estructura D3DXMATRIX que es la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-138">Pointer to a D3DXMATRIX structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad4ce-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad4ce-139">Remarks</span></span>

<span data-ttu-id="ad4ce-140">Esta función calcula la matriz de transformación con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="ad4ce-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="ad4ce-141">M<sub>out</sub> = (M<sub>sc</sub>)/¹ \* (M<sub>sr</sub>)/ntes \* \* Ms M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> M \* <sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="ad4ce-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="ad4ce-142">donde:</span><span class="sxs-lookup"><span data-stu-id="ad4ce-142">where:</span></span>

<span data-ttu-id="ad4ce-143">M<sub>out</sub> = matriz de salida (pOut)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-143">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="ad4ce-144">M<sub>sc</sub> = matriz del centro de escalado (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-144">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="ad4ce-145">M<sub>sr</sub> = matriz de rotación de escalado (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-145">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="ad4ce-146">Ms = matriz de escalado (pScaling)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-146">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="ad4ce-147">M<sub>rc</sub> = centro de la matriz de rotación (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-147">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="ad4ce-148">M<sub>r</sub> = matriz de rotación (pRotation)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-148">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="ad4ce-149">Mt = matriz de traducción (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-149">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="ad4ce-150">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-150">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ad4ce-151">De esta manera, la función D3DXMatrixTransformation se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-151">In this way, the D3DXMatrixTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ad4ce-152">Para las transformaciones 2D, use [**D3DXMatrixTransformation2D.**](d3d10-d3dxmatrixtransformation2d.md)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad4ce-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad4ce-153">Requirements</span></span>



| <span data-ttu-id="ad4ce-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad4ce-154">Requirement</span></span> | <span data-ttu-id="ad4ce-155">Value</span><span class="sxs-lookup"><span data-stu-id="ad4ce-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4ce-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad4ce-156">Header</span></span><br/>  | <dl> <span data-ttu-id="ad4ce-157"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ce-157"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ad4ce-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad4ce-158">Library</span></span><br/> | <dl> <span data-ttu-id="ad4ce-159"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ce-159"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad4ce-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad4ce-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4ce-161">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="ad4ce-161">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
