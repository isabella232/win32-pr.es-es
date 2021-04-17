---
description: Crea una matriz de transformación afín 3D. Los argumentos NULL se tratan como transformaciones de identidad.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Función D3DXMatrixAffineTransformation (D3DX10Math. h)
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
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698371"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="b914c-104">Función D3DXMatrixAffineTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b914c-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="b914c-105">Crea una matriz de transformación afín 3D.</span><span class="sxs-lookup"><span data-stu-id="b914c-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="b914c-106">Los argumentos **null** se tratan como transformaciones de identidad.</span><span class="sxs-lookup"><span data-stu-id="b914c-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b914c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b914c-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="b914c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b914c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b914c-109">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b914c-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b914c-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b914c-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b914c-111">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b914c-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b914c-112">*Escalado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b914c-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b914c-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b914c-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b914c-114">Factor de escala.</span><span class="sxs-lookup"><span data-stu-id="b914c-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="b914c-115">*pRotationCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b914c-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b914c-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b914c-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b914c-117">Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), un punto que identifica el centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="b914c-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="b914c-118">Si este argumento es **null**, se aplica una matriz identidad M <sub>RC</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b914c-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b914c-119">*Prot.* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b914c-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b914c-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b914c-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b914c-121">Puntero a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica la rotación.</span><span class="sxs-lookup"><span data-stu-id="b914c-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="b914c-122">Si este argumento es **null**, se aplica una matriz de identidad M <sub>r</sub> a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b914c-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b914c-123">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b914c-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b914c-124">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b914c-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b914c-125">Puntero a una estructura D3DXVECTOR3 que representa la traslación.</span><span class="sxs-lookup"><span data-stu-id="b914c-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="b914c-126">Si este argumento es **null**, se aplica una matriz Identity MT a la fórmula en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b914c-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b914c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b914c-127">Return value</span></span>

<span data-ttu-id="b914c-128">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b914c-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b914c-129">Puntero a una estructura D3DXMATRIX que es una matriz de transformación afín.</span><span class="sxs-lookup"><span data-stu-id="b914c-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b914c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b914c-130">Remarks</span></span>

<span data-ttu-id="b914c-131">Esta función calcula la matriz de transformación afín con la fórmula siguiente, con la concatenación de matriz evaluada en orden de izquierda a derecha:</span><span class="sxs-lookup"><span data-stu-id="b914c-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="b914c-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="b914c-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="b914c-133">donde:</span><span class="sxs-lookup"><span data-stu-id="b914c-133">where:</span></span>

<span data-ttu-id="b914c-134">M<sub>out</sub> = matriz de salida (pOut)</span><span class="sxs-lookup"><span data-stu-id="b914c-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="b914c-135">MS = matriz de escalado (escala)</span><span class="sxs-lookup"><span data-stu-id="b914c-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="b914c-136">M<sub>RC</sub> = centro de la matriz de rotación (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="b914c-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="b914c-137">M<sub>r</sub> = matriz de rotación (Prot.)</span><span class="sxs-lookup"><span data-stu-id="b914c-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="b914c-138">MT = matriz de traslación (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="b914c-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="b914c-139">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b914c-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b914c-140">De esta manera, la función D3DXMatrixAffineTransformation se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="b914c-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b914c-141">En el caso de las transformaciones afines de 2D, use D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="b914c-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="b914c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b914c-142">Requirements</span></span>



| <span data-ttu-id="b914c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b914c-143">Requirement</span></span> | <span data-ttu-id="b914c-144">Value</span><span class="sxs-lookup"><span data-stu-id="b914c-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b914c-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b914c-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b914c-146"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b914c-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b914c-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b914c-147">Library</span></span><br/> | <dl> <span data-ttu-id="b914c-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b914c-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b914c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="b914c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b914c-150">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b914c-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
