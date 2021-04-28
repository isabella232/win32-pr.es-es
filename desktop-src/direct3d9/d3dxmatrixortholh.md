---
description: 'Función D3DXMatrixOrthoLH (D3dx9math.h): crea una matriz de proyección ortográfica de mano izquierda.'
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Función D3DXMatrixOrthoLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107503"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="fda8a-103">Función D3DXMatrixOrthoLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fda8a-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="fda8a-104">Crea una matriz de proyección ortográfica a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="fda8a-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fda8a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="fda8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fda8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda8a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fda8a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda8a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fda8a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fda8a-109">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="fda8a-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="fda8a-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fda8a-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda8a-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fda8a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fda8a-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="fda8a-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fda8a-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fda8a-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda8a-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fda8a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fda8a-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="fda8a-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="fda8a-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fda8a-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda8a-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fda8a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fda8a-118">Valor z mínimo del volumen de vista que se conoce como z-near.</span><span class="sxs-lookup"><span data-stu-id="fda8a-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="fda8a-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fda8a-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda8a-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fda8a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fda8a-121">Valor z máximo del volumen de vista que se conoce como z-far.</span><span class="sxs-lookup"><span data-stu-id="fda8a-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda8a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fda8a-122">Return value</span></span>

<span data-ttu-id="fda8a-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fda8a-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fda8a-124">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="fda8a-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fda8a-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fda8a-125">Remarks</span></span>

<span data-ttu-id="fda8a-126">Todos los parámetros de la **función D3DXMatrixOrthoLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="fda8a-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="fda8a-127">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="fda8a-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="fda8a-128">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="fda8a-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fda8a-129">De este modo, la **función D3DXMatrixOrthoLH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="fda8a-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fda8a-130">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="fda8a-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="fda8a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fda8a-131">Requirements</span></span>



| <span data-ttu-id="fda8a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fda8a-132">Requirement</span></span> | <span data-ttu-id="fda8a-133">Value</span><span class="sxs-lookup"><span data-stu-id="fda8a-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fda8a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fda8a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fda8a-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fda8a-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fda8a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fda8a-136">Library</span></span><br/> | <dl> <span data-ttu-id="fda8a-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fda8a-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fda8a-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fda8a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda8a-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fda8a-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fda8a-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="fda8a-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="fda8a-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="fda8a-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="fda8a-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="fda8a-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
