---
description: Crea una matriz de transformación 2D que representa las transformaciones en el plano XY. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Función D3DXMatrixTransformation2D (D3DX10Math. h)
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
ms.openlocfilehash: b41d8234dcd9dda1b3735c83460a20c7109e63d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821386"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a><span data-ttu-id="3740a-104">Función D3DXMatrixTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3740a-104">D3DXMatrixTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="3740a-105">Crea una matriz de transformación 2D que representa las transformaciones en el plano XY.</span><span class="sxs-lookup"><span data-stu-id="3740a-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="3740a-106">Los argumentos **null** se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="3740a-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="3740a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3740a-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3740a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3740a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3740a-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3740a-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3740a-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3740a-111">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que contiene el resultado de las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="3740a-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-112">*pScalingCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-113">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3740a-113">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="3740a-114">Puntero a un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), un punto que identifica el centro de escalado.</span><span class="sxs-lookup"><span data-stu-id="3740a-114">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the scaling center.</span></span> <span data-ttu-id="3740a-115">Si este argumento es **null**, se aplica una matriz identidad M <sub>SC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3740a-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-116">*ScalingRotation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-116">*ScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3740a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3740a-118">Puntero al factor de rotación de escalado.</span><span class="sxs-lookup"><span data-stu-id="3740a-118">Pointer to the scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-119">*pScaling* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3740a-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="3740a-121">Puntero a una estructura D3DXVECTOR2, un punto que identifica la escala.</span><span class="sxs-lookup"><span data-stu-id="3740a-121">Pointer to a D3DXVECTOR2 structure, a point identifying the scale.</span></span> <span data-ttu-id="3740a-122">Si este argumento es **null**, se aplica una matriz de identidad MS a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3740a-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-123">*pRotationCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-124">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3740a-124">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="3740a-125">Puntero a una estructura D3DXVECTOR2, un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="3740a-125">Pointer to a D3DXVECTOR2 structure, a point identifying the rotation center.</span></span> <span data-ttu-id="3740a-126">Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3740a-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-127">*Giro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-128">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3740a-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3740a-129">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="3740a-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="3740a-130">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3740a-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3740a-131">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3740a-131">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="3740a-132">Puntero a una estructura D3DXVECTOR2, que identifica la traducción.</span><span class="sxs-lookup"><span data-stu-id="3740a-132">Pointer to a D3DXVECTOR2 structure, identifying the translation.</span></span> <span data-ttu-id="3740a-133">Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3740a-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3740a-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3740a-134">Return value</span></span>

<span data-ttu-id="3740a-135">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3740a-135">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3740a-136">Puntero a una estructura D3DXMATRIX que contiene la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="3740a-136">Pointer to a D3DXMATRIX structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="3740a-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3740a-137">Remarks</span></span>

<span data-ttu-id="3740a-138">Esta función calcula la matriz de transformación con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="3740a-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="3740a-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="3740a-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="3740a-140">donde:</span><span class="sxs-lookup"><span data-stu-id="3740a-140">where:</span></span>

<span data-ttu-id="3740a-141">M<sub>out</sub> = matriz de salida (pOut)</span><span class="sxs-lookup"><span data-stu-id="3740a-141">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="3740a-142">M<sub>SC</sub> = matriz de centro de escalado (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="3740a-142">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="3740a-143">M<sub>Sr</sub> = matriz de rotación de escala (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="3740a-143">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="3740a-144">MS = matriz de escalado (pScaling)</span><span class="sxs-lookup"><span data-stu-id="3740a-144">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="3740a-145">M<sub>RC</sub> = centro de la matriz de rotación (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="3740a-145">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="3740a-146">M<sub>r</sub> = matriz de rotación (giro)</span><span class="sxs-lookup"><span data-stu-id="3740a-146">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="3740a-147">MT = matriz de traslación (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="3740a-147">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="3740a-148">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3740a-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3740a-149">De esta manera, la función D3DXMatrixTransformation2D se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="3740a-149">In this way, the D3DXMatrixTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3740a-150">Para las transformaciones 3D, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="3740a-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3740a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3740a-151">Requirements</span></span>



| <span data-ttu-id="3740a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="3740a-152">Requirement</span></span> | <span data-ttu-id="3740a-153">Value</span><span class="sxs-lookup"><span data-stu-id="3740a-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3740a-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3740a-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3740a-155"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3740a-155"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3740a-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3740a-156">Library</span></span><br/> | <dl> <span data-ttu-id="3740a-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3740a-157"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3740a-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="3740a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3740a-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3740a-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
