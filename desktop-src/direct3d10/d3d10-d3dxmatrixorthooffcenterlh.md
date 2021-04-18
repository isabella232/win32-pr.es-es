---
description: Crea una matriz de proyección ortográfica personalizada y de mano izquierda.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Función D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4292f2996b4a19b71531094e5bf39bf7c213b972
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721496"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="873f2-103">Función D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="873f2-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="873f2-104">Crea una matriz de proyección ortográfica personalizada y de mano izquierda.</span><span class="sxs-lookup"><span data-stu-id="873f2-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="873f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="873f2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="873f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="873f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="873f2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="873f2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="873f2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="873f2-109">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="873f2-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="873f2-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="873f2-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="873f2-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="873f2-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="873f2-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="873f2-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="873f2-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="873f2-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="873f2-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="873f2-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="873f2-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="873f2-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873f2-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873f2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="873f2-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="873f2-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="873f2-128">Return value</span></span>

<span data-ttu-id="873f2-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="873f2-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="873f2-130">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="873f2-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="873f2-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="873f2-131">Remarks</span></span>

<span data-ttu-id="873f2-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) es un caso especial de la función D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="873f2-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="873f2-133">Para crear la misma proyección mediante D3DXMatrixOrthoOffCenterLH, use los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="873f2-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="873f2-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="873f2-134">l = -w/2,</span></span>

<span data-ttu-id="873f2-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="873f2-135">r = w/2,</span></span>

<span data-ttu-id="873f2-136">b =-h/2 y</span><span class="sxs-lookup"><span data-stu-id="873f2-136">b = -h/2, and</span></span>

<span data-ttu-id="873f2-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="873f2-137">t = h/2.</span></span>

<span data-ttu-id="873f2-138">Todos los parámetros de la función D3DXMatrixOrthoOffCenterLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="873f2-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="873f2-139">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="873f2-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="873f2-140">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="873f2-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="873f2-141">De esta manera, la función D3DXMatrixOrthoOffCenterLH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="873f2-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="873f2-142">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="873f2-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="873f2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="873f2-143">Requirements</span></span>



| <span data-ttu-id="873f2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="873f2-144">Requirement</span></span> | <span data-ttu-id="873f2-145">Value</span><span class="sxs-lookup"><span data-stu-id="873f2-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="873f2-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="873f2-146">Header</span></span><br/>  | <dl> <span data-ttu-id="873f2-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="873f2-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="873f2-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="873f2-148">Library</span></span><br/> | <dl> <span data-ttu-id="873f2-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="873f2-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="873f2-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="873f2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873f2-151">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="873f2-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
