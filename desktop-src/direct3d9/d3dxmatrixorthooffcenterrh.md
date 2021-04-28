---
description: 'Función D3DXMatrixOrthoOffCenterRH (D3dx9math.h): crea una matriz de proyección ortográfica con la mano derecha personalizada.'
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Función D3DXMatrixOrthoOffCenterRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107463"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="edfd6-103">Función D3DXMatrixOrthoOffCenterRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="edfd6-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="edfd6-104">Crea una matriz de proyección ortográfica personalizada y con la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="edfd6-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="edfd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edfd6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="edfd6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edfd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edfd6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="edfd6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="edfd6-109">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="edfd6-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-118">Valor Y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-121">Valor Y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-122">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-124">Valor Z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="edfd6-125">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="edfd6-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edfd6-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edfd6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edfd6-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edfd6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edfd6-128">Return value</span></span>

<span data-ttu-id="edfd6-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="edfd6-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="edfd6-130">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="edfd6-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="edfd6-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edfd6-131">Remarks</span></span>

<span data-ttu-id="edfd6-132">La [**función D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) es un caso especial de la función **D3DXMatrixOrthoOffCenterRH.**</span><span class="sxs-lookup"><span data-stu-id="edfd6-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="edfd6-133">Para crear la misma proyección con **D3DXMatrixOrthoOffCenterRH,** use los valores siguientes: l = -w/2, r = w/2, b = -h/2 y t = h/2.</span><span class="sxs-lookup"><span data-stu-id="edfd6-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="edfd6-134">Todos los parámetros de la **función D3DXMatrixOrthoOffCenterRH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="edfd6-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="edfd6-135">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="edfd6-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="edfd6-136">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="edfd6-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="edfd6-137">De este modo, la **función D3DXMatrixOrthoOffCenterRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="edfd6-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="edfd6-138">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="edfd6-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="edfd6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edfd6-139">Requirements</span></span>



| <span data-ttu-id="edfd6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="edfd6-140">Requirement</span></span> | <span data-ttu-id="edfd6-141">Value</span><span class="sxs-lookup"><span data-stu-id="edfd6-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edfd6-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edfd6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="edfd6-143"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="edfd6-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="edfd6-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edfd6-144">Library</span></span><br/> | <dl> <span data-ttu-id="edfd6-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="edfd6-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="edfd6-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edfd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edfd6-147">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="edfd6-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="edfd6-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="edfd6-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="edfd6-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="edfd6-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="edfd6-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="edfd6-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
