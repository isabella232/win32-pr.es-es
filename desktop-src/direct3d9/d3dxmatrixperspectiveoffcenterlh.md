---
description: Crea una matriz de proyección de perspectiva personalizada y diestro.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Función D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)
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
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717571"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="7c0f6-103">Función D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7c0f6-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="7c0f6-104">Crea una matriz de proyección de perspectiva personalizada y diestro.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c0f6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7c0f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c0f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0f6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c0f6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c0f6-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c0f6-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c0f6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c0f6-128">Return value</span></span>

<span data-ttu-id="7c0f6-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c0f6-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c0f6-130">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz personalizada de proyección de perspectiva que se ha personalizado.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0f6-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c0f6-131">Remarks</span></span>

<span data-ttu-id="7c0f6-132">Todos los parámetros de la función **D3DXMatrixPerspectiveOffCenterLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="7c0f6-133">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="7c0f6-134">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="7c0f6-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7c0f6-135">De esta manera, la función **D3DXMatrixPerspectiveOffCenterLH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7c0f6-136">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="7c0f6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0f6-137">Requirements</span></span>



| <span data-ttu-id="7c0f6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0f6-138">Requirement</span></span> | <span data-ttu-id="7c0f6-139">Value</span><span class="sxs-lookup"><span data-stu-id="7c0f6-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0f6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c0f6-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7c0f6-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0f6-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7c0f6-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c0f6-142">Library</span></span><br/> | <dl> <span data-ttu-id="7c0f6-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c0f6-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c0f6-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c0f6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0f6-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7c0f6-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7c0f6-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="7c0f6-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="7c0f6-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="7c0f6-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="7c0f6-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
