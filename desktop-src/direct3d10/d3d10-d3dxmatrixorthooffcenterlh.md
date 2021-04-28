---
description: 'Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h): crea una matriz de proyección ortográfica a la izquierda personalizada.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)
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
ms.openlocfilehash: 2eb10963372519827eb544371ebb0df04df2e178
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109143"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="d5882-103">Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d5882-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d5882-104">Crea una matriz de proyección ortográfica a la izquierda personalizada.</span><span class="sxs-lookup"><span data-stu-id="d5882-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5882-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5882-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d5882-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5882-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5882-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5882-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d5882-109">Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d5882-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5882-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5882-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-112">Valor X mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5882-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5882-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5882-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5882-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-118">Valor Y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5882-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5882-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-121">Valor Y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5882-122">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d5882-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5882-125">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d5882-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5882-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5882-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5882-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5882-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5882-128">Return value</span></span>

<span data-ttu-id="d5882-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5882-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d5882-130">Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d5882-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5882-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5882-131">Remarks</span></span>

<span data-ttu-id="d5882-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) es un caso especial de la función D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="d5882-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="d5882-133">Para crear la misma proyección mediante D3DXMatrixOrthoOffCenterLH, use los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5882-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="d5882-134">l = -w/2,</span><span class="sxs-lookup"><span data-stu-id="d5882-134">l = -w/2,</span></span>

<span data-ttu-id="d5882-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="d5882-135">r = w/2,</span></span>

<span data-ttu-id="d5882-136">b = -h/2 y</span><span class="sxs-lookup"><span data-stu-id="d5882-136">b = -h/2, and</span></span>

<span data-ttu-id="d5882-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="d5882-137">t = h/2.</span></span>

<span data-ttu-id="d5882-138">Todos los parámetros de la función D3DXMatrixOrthoOffCenterLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="d5882-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="d5882-139">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="d5882-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d5882-140">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d5882-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d5882-141">De esta manera, la función D3DXMatrixOrthoOffCenterLH se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="d5882-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d5882-142">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="d5882-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="d5882-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5882-143">Requirements</span></span>



| <span data-ttu-id="d5882-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5882-144">Requirement</span></span> | <span data-ttu-id="d5882-145">Value</span><span class="sxs-lookup"><span data-stu-id="d5882-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5882-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5882-146">Header</span></span><br/>  | <dl> <span data-ttu-id="d5882-147"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d5882-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d5882-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5882-148">Library</span></span><br/> | <dl> <span data-ttu-id="d5882-149"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5882-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5882-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5882-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5882-151">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d5882-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
