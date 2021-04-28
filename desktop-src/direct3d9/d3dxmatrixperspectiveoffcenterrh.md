---
description: 'Función D3DXMatrixPerspectiveOffCenterRH (D3dx9math.h): crea una matriz de proyección de perspectiva personalizada y derecha.'
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: Función D3DXMatrixPerspectiveOffCenterRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d051894a6706cf8d58b81a85003666513f2a956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118283"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="024c6-103">Función D3DXMatrixPerspectiveOffCenterRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="024c6-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="024c6-104">Crea una matriz de proyección de perspectiva personalizada y con la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="024c6-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="024c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="024c6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="024c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="024c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024c6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="024c6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="024c6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="024c6-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="024c6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="024c6-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-112">Valor X mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="024c6-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="024c6-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-118">Valor Y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="024c6-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-121">Valor Y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-122">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="024c6-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-125">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="024c6-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c6-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="024c6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="024c6-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024c6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="024c6-128">Return value</span></span>

<span data-ttu-id="024c6-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="024c6-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="024c6-130">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva personalizada y a la derecha.</span><span class="sxs-lookup"><span data-stu-id="024c6-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="024c6-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="024c6-131">Remarks</span></span>

<span data-ttu-id="024c6-132">Todos los parámetros de la **función D3DXMatrixPerspectiveOffCenterRH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="024c6-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="024c6-133">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="024c6-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="024c6-134">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="024c6-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="024c6-135">De esta manera, la función **D3DXMatrixPerspectiveOffCenterRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="024c6-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="024c6-136">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="024c6-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="024c6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024c6-137">Requirements</span></span>



| <span data-ttu-id="024c6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="024c6-138">Requirement</span></span> | <span data-ttu-id="024c6-139">Value</span><span class="sxs-lookup"><span data-stu-id="024c6-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="024c6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="024c6-140">Header</span></span><br/>  | <dl> <span data-ttu-id="024c6-141"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="024c6-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="024c6-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="024c6-142">Library</span></span><br/> | <dl> <span data-ttu-id="024c6-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="024c6-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="024c6-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="024c6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024c6-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="024c6-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="024c6-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="024c6-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="024c6-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="024c6-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="024c6-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="024c6-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="024c6-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="024c6-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="024c6-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="024c6-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
