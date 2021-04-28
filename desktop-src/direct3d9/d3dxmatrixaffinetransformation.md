---
description: 'Función D3DXMatrixAffineTransformation (D3dx9math.h): crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Función D3DXMatrixAffineTransformation (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094173"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="13aa8-104">Función D3DXMatrixAffineTransformation (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="13aa8-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="13aa8-105">Crea una matriz de transformación afín 3D.</span><span class="sxs-lookup"><span data-stu-id="13aa8-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="13aa8-106">**Los** argumentos NULL se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="13aa8-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="13aa8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13aa8-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="13aa8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13aa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13aa8-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13aa8-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13aa8-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="13aa8-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="13aa8-111">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="13aa8-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13aa8-112">*Escalado* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13aa8-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13aa8-113">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13aa8-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13aa8-114">Factor de escalado.</span><span class="sxs-lookup"><span data-stu-id="13aa8-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="13aa8-115">*pRotationCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13aa8-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13aa8-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="13aa8-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="13aa8-117">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="13aa8-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="13aa8-118">Si este argumento es **NULL,** se aplica una matriz M <sub>rc</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13aa8-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="13aa8-119">*pRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13aa8-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13aa8-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="13aa8-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="13aa8-121">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="13aa8-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="13aa8-122">Si este argumento es **NULL,** se aplica una matriz <sub>M r</sub> de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13aa8-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="13aa8-123">*pTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13aa8-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13aa8-124">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="13aa8-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="13aa8-125">Puntero a una [**estructura D3DXVECTOR3 que**](d3dxvector3.md) representa la traducción.</span><span class="sxs-lookup"><span data-stu-id="13aa8-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="13aa8-126">Si este argumento es **NULL,** se aplica una matriz mt de identidad a la fórmula en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13aa8-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13aa8-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13aa8-127">Return value</span></span>

<span data-ttu-id="13aa8-128">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="13aa8-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="13aa8-129">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de transformación afín.</span><span class="sxs-lookup"><span data-stu-id="13aa8-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="13aa8-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13aa8-130">Remarks</span></span>

<span data-ttu-id="13aa8-131">Esta función calcula la matriz de transformación afín con la siguiente fórmula, con la concatenación de matrices evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="13aa8-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="13aa8-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)/¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="13aa8-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="13aa8-133">donde:</span><span class="sxs-lookup"><span data-stu-id="13aa8-133">where:</span></span>

<span data-ttu-id="13aa8-134">M <sub>out</sub> = matriz de salida (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="13aa8-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="13aa8-135">Ms = matriz de escalado (*escalado*)</span><span class="sxs-lookup"><span data-stu-id="13aa8-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="13aa8-136">M <sub>rc</sub> = centro de la matriz de rotación (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="13aa8-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="13aa8-137">M <sub>r</sub> = matriz de rotación (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="13aa8-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="13aa8-138">Mt = matriz de traducción (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="13aa8-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="13aa8-139">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="13aa8-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="13aa8-140">De este modo, la **función D3DXMatrixAffineTransformation** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="13aa8-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="13aa8-141">Para las transformaciones de afín 2D, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="13aa8-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13aa8-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13aa8-142">Requirements</span></span>



| <span data-ttu-id="13aa8-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="13aa8-143">Requirement</span></span> | <span data-ttu-id="13aa8-144">Value</span><span class="sxs-lookup"><span data-stu-id="13aa8-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13aa8-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13aa8-145">Header</span></span><br/>  | <dl> <span data-ttu-id="13aa8-146"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="13aa8-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="13aa8-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13aa8-147">Library</span></span><br/> | <dl> <span data-ttu-id="13aa8-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="13aa8-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13aa8-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13aa8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13aa8-150">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="13aa8-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="13aa8-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="13aa8-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="13aa8-152">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="13aa8-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
