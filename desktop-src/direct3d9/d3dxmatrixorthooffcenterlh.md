---
description: 'Función D3DXMatrixOrthoOffCenterLH (D3dx9math.h): crea una matriz de proyección ortográfica a la izquierda personalizada.'
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Función D3DXMatrixOrthoOffCenterLH (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 704bdab1d486399b28117cd078f556beb1347f7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107493"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="e4ade-103">Función D3DXMatrixOrthoOffCenterLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e4ade-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="e4ade-104">Crea una matriz de proyección ortográfica personalizada y a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="e4ade-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ade-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4ade-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e4ade-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ade-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4ade-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4ade-109">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="e4ade-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-118">Valor Y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-121">Valor Y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-122">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e4ade-125">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e4ade-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ade-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4ade-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4ade-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ade-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4ade-128">Return value</span></span>

<span data-ttu-id="e4ade-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4ade-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4ade-130">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="e4ade-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ade-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4ade-131">Remarks</span></span>

<span data-ttu-id="e4ade-132">La [**función D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) es un caso especial de la función **D3DXMatrixOrthoOffCenterLH.**</span><span class="sxs-lookup"><span data-stu-id="e4ade-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="e4ade-133">Para crear la misma proyección con **D3DXMatrixOrthoOffCenterLH,** use los valores siguientes: l = -w/2, r = w/2, b = -h/2 y t = h/2.</span><span class="sxs-lookup"><span data-stu-id="e4ade-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="e4ade-134">Todos los parámetros de la **función D3DXMatrixOrthoOffCenterLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="e4ade-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="e4ade-135">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="e4ade-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="e4ade-136">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="e4ade-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e4ade-137">De este modo, la **función D3DXMatrixOrthoOffCenterLH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e4ade-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e4ade-138">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="e4ade-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="e4ade-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ade-139">Requirements</span></span>



| <span data-ttu-id="e4ade-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ade-140">Requirement</span></span> | <span data-ttu-id="e4ade-141">Value</span><span class="sxs-lookup"><span data-stu-id="e4ade-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ade-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4ade-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ade-143"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4ade-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4ade-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4ade-144">Library</span></span><br/> | <dl> <span data-ttu-id="e4ade-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4ade-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4ade-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4ade-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ade-147">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e4ade-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4ade-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="e4ade-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="e4ade-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="e4ade-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="e4ade-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="e4ade-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
