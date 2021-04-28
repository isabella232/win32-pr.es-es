---
description: 'Función D3DXMatrixPerspectiveOffCenterLH (D3dx9math.h): crea una matriz de proyección de perspectiva personalizada y con la mano izquierda.'
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Función D3DXMatrixPerspectiveOffCenterLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 404147cfbab0b4fedb7c7356dc1c31d3e203eb5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118293"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="6da21-103">Función D3DXMatrixPerspectiveOffCenterLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6da21-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="6da21-104">Crea una matriz de proyección de perspectiva personalizada y con la mano izquierda.</span><span class="sxs-lookup"><span data-stu-id="6da21-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6da21-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="6da21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6da21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da21-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6da21-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6da21-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6da21-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6da21-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6da21-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-112">Valor X mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6da21-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6da21-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-118">Valor Y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da21-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-121">Valor Y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-122">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6da21-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-124">Valor Z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6da21-125">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6da21-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da21-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da21-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da21-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da21-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6da21-128">Return value</span></span>

<span data-ttu-id="6da21-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6da21-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6da21-130">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva a la izquierda personalizada.</span><span class="sxs-lookup"><span data-stu-id="6da21-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6da21-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6da21-131">Remarks</span></span>

<span data-ttu-id="6da21-132">Todos los parámetros de la **función D3DXMatrixPerspectiveOffCenterLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="6da21-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="6da21-133">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="6da21-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="6da21-134">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="6da21-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6da21-135">De este modo, la **función D3DXMatrixPerspectiveOffCenterLH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="6da21-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6da21-136">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="6da21-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="6da21-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6da21-137">Requirements</span></span>



| <span data-ttu-id="6da21-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da21-138">Requirement</span></span> | <span data-ttu-id="6da21-139">Value</span><span class="sxs-lookup"><span data-stu-id="6da21-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da21-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6da21-140">Header</span></span><br/>  | <dl> <span data-ttu-id="6da21-141"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6da21-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6da21-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6da21-142">Library</span></span><br/> | <dl> <span data-ttu-id="6da21-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6da21-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6da21-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6da21-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da21-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6da21-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6da21-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="6da21-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="6da21-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="6da21-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="6da21-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="6da21-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="6da21-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="6da21-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="6da21-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="6da21-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
