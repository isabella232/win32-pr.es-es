---
description: Crea una matriz de transformación 2D que representa las transformaciones en el plano XY. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Función D3DXMatrixTransformation2D (D3dx9math. h)
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
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717753"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="4ae14-104">Función D3DXMatrixTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4ae14-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="4ae14-105">Crea una matriz de transformación 2D que representa las transformaciones en el plano XY.</span><span class="sxs-lookup"><span data-stu-id="4ae14-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="4ae14-106">Los argumentos **null** se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="4ae14-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae14-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ae14-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4ae14-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ae14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae14-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae14-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4ae14-111">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene el resultado de las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="4ae14-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-112">*pScalingCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-113">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ae14-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4ae14-114">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de escalado.</span><span class="sxs-lookup"><span data-stu-id="4ae14-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="4ae14-115">Si este argumento es **null**, se aplica una matriz identidad M <sub>SC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4ae14-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-116">*pScalingRotation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae14-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ae14-118">Factor de rotación de escala.</span><span class="sxs-lookup"><span data-stu-id="4ae14-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-119">*pScaling* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-120">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ae14-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4ae14-121">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica la escala.</span><span class="sxs-lookup"><span data-stu-id="4ae14-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="4ae14-122">Si este argumento es **null**, se aplica una matriz de identidad MS a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4ae14-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-123">*pRotationCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-124">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ae14-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4ae14-125">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="4ae14-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="4ae14-126">Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4ae14-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-127">*Giro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-128">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae14-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ae14-129">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="4ae14-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4ae14-130">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ae14-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae14-131">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ae14-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4ae14-132">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , que identifica la traducción.</span><span class="sxs-lookup"><span data-stu-id="4ae14-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="4ae14-133">Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4ae14-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae14-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ae14-134">Return value</span></span>

<span data-ttu-id="4ae14-135">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae14-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4ae14-136">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="4ae14-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae14-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ae14-137">Remarks</span></span>

<span data-ttu-id="4ae14-138">Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="4ae14-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="4ae14-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="4ae14-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="4ae14-140">donde:</span><span class="sxs-lookup"><span data-stu-id="4ae14-140">where:</span></span>

<span data-ttu-id="4ae14-141">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="4ae14-142">M <sub>SC</sub> = matriz de centro de escalado (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="4ae14-143">M <sub>Sr</sub> = matriz de rotación de escala (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="4ae14-144">MS = matriz de escalado (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="4ae14-145">M <sub>RC</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="4ae14-146">M <sub>r</sub> = matriz de rotación (*giro*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="4ae14-147">MT = matriz de traslación (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="4ae14-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="4ae14-148">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="4ae14-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4ae14-149">De esta manera, la función **D3DXMatrixTransformation2D** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="4ae14-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4ae14-150">Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="4ae14-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae14-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae14-151">Requirements</span></span>



| <span data-ttu-id="4ae14-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae14-152">Requirement</span></span> | <span data-ttu-id="4ae14-153">Value</span><span class="sxs-lookup"><span data-stu-id="4ae14-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae14-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae14-154">Header</span></span><br/>  | <dl> <span data-ttu-id="4ae14-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae14-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4ae14-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ae14-156">Library</span></span><br/> | <dl> <span data-ttu-id="4ae14-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ae14-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ae14-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ae14-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae14-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4ae14-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4ae14-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="4ae14-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="4ae14-161">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ae14-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
