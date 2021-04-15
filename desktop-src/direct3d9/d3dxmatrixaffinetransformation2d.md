---
description: Crea una matriz de transformación afín 2D en el plano XY. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Función D3DXMatrixAffineTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707837"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="503a5-104">Función D3DXMatrixAffineTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="503a5-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="503a5-105">Crea una matriz de transformación afín 2D en el plano XY.</span><span class="sxs-lookup"><span data-stu-id="503a5-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="503a5-106">Los argumentos **null** se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="503a5-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="503a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="503a5-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="503a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="503a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="503a5-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="503a5-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="503a5-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="503a5-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="503a5-111">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="503a5-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="503a5-112">*Escalado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="503a5-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503a5-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="503a5-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="503a5-114">Factor de escala.</span><span class="sxs-lookup"><span data-stu-id="503a5-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="503a5-115">*pRotationCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="503a5-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503a5-116">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="503a5-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="503a5-117">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) , un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="503a5-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="503a5-118">Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="503a5-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="503a5-119">*Giro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="503a5-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503a5-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="503a5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="503a5-121">Ángulo de rotación.</span><span class="sxs-lookup"><span data-stu-id="503a5-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="503a5-122">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="503a5-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503a5-123">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="503a5-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="503a5-124">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que representa la traslación.</span><span class="sxs-lookup"><span data-stu-id="503a5-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="503a5-125">Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="503a5-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="503a5-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="503a5-126">Return value</span></span>

<span data-ttu-id="503a5-127">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="503a5-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="503a5-128">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz de transformación afín.</span><span class="sxs-lookup"><span data-stu-id="503a5-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="503a5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="503a5-129">Remarks</span></span>

<span data-ttu-id="503a5-130">Esta función calcula la matriz de transformación afín con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="503a5-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="503a5-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="503a5-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="503a5-132">donde:</span><span class="sxs-lookup"><span data-stu-id="503a5-132">where:</span></span>

<span data-ttu-id="503a5-133">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="503a5-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="503a5-134">MS = matriz de escalado (*escala*)</span><span class="sxs-lookup"><span data-stu-id="503a5-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="503a5-135">M <sub>RC</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="503a5-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="503a5-136">M <sub>r</sub> = matriz de rotación (*giro*)</span><span class="sxs-lookup"><span data-stu-id="503a5-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="503a5-137">MT = matriz de traslación (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="503a5-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="503a5-138">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="503a5-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="503a5-139">De esta manera, la función **D3DXMatrixAffineTransformation2D** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="503a5-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="503a5-140">En el caso de las transformaciones afines 3D, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="503a5-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="503a5-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="503a5-141">Requirements</span></span>



| <span data-ttu-id="503a5-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="503a5-142">Requirement</span></span> | <span data-ttu-id="503a5-143">Value</span><span class="sxs-lookup"><span data-stu-id="503a5-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="503a5-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="503a5-144">Header</span></span><br/>  | <dl> <span data-ttu-id="503a5-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="503a5-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="503a5-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="503a5-146">Library</span></span><br/> | <dl> <span data-ttu-id="503a5-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="503a5-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="503a5-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="503a5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503a5-149">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="503a5-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="503a5-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="503a5-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="503a5-151">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="503a5-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
