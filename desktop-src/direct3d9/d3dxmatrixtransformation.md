---
description: Crea una matriz de transformación. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Función D3DXMatrixTransformation (D3dx9math. h)
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
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083704"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="f6fb9-104">Función D3DXMatrixTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="f6fb9-105">Crea una matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-105">Builds a transformation matrix.</span></span> <span data-ttu-id="f6fb9-106">Los argumentos **null** se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fb9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6fb9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f6fb9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6fb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fb9-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f6fb9-111">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-112">*pScalingCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f6fb9-114">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que identifica el punto central de escalado.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="f6fb9-115">Si este argumento es **null**, se aplica una matriz identidad M <sub>SC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-116">*pScalingRotation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f6fb9-118">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación del escalado.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="f6fb9-119">Si este argumento es **null**, se aplica una matriz de identidad M <sub>Sr</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-120">*pScaling* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f6fb9-122">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , el vector de escala.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="f6fb9-123">Si este argumento es **null**, se aplica una matriz de identidad MS a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-124">*pRotationCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-125">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f6fb9-126">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="f6fb9-127">Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-128">*Prot.* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-129">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f6fb9-130">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="f6fb9-131">Si este argumento es **null**, se aplica una matriz de identidad M <sub>r</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6fb9-132">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6fb9-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fb9-133">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f6fb9-134">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que representa la traslación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="f6fb9-135">Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fb9-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6fb9-136">Return value</span></span>

<span data-ttu-id="f6fb9-137">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6fb9-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f6fb9-138">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6fb9-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6fb9-139">Remarks</span></span>

<span data-ttu-id="f6fb9-140">Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="f6fb9-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f6fb9-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="f6fb9-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="f6fb9-142">donde:</span><span class="sxs-lookup"><span data-stu-id="f6fb9-142">where:</span></span>

<span data-ttu-id="f6fb9-143">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="f6fb9-144">M <sub>SC</sub> = matriz de centro de escalado (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="f6fb9-145">M <sub>Sr</sub> = matriz de rotación de escala (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="f6fb9-146">MS = matriz de escalado (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="f6fb9-147">M <sub>RC</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="f6fb9-148">M <sub>r</sub> = matriz de rotación (*Prot*.)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="f6fb9-149">MT = matriz de traslación (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="f6fb9-150">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="f6fb9-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f6fb9-151">De esta manera, la función **D3DXMatrixTransformation** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f6fb9-152">Para las transformaciones 2D, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="f6fb9-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fb9-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6fb9-153">Requirements</span></span>



| <span data-ttu-id="f6fb9-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6fb9-154">Requirement</span></span> | <span data-ttu-id="f6fb9-155">Value</span><span class="sxs-lookup"><span data-stu-id="f6fb9-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fb9-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6fb9-156">Header</span></span><br/>  | <dl> <span data-ttu-id="f6fb9-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6fb9-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f6fb9-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6fb9-158">Library</span></span><br/> | <dl> <span data-ttu-id="f6fb9-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6fb9-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6fb9-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6fb9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fb9-161">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f6fb9-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f6fb9-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="f6fb9-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="f6fb9-163">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f6fb9-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




