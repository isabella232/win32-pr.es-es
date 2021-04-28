---
description: 'Función D3DXMatrixPerspectiveRH (D3dx9math.h): crea una matriz de proyección de perspectiva con la mano derecha.'
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Función D3DXMatrixPerspectiveRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3c583b74366a0a00054bbeced1ece2bd3d1c1cd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118243"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="fd7b3-103">Función D3DXMatrixPerspectiveRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fd7b3-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="fd7b3-104">Crea una matriz de proyección de perspectiva a la derecha.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd7b3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="fd7b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd7b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7b3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd7b3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7b3-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd7b3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd7b3-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd7b3-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7b3-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7b3-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd7b3-112">Ancho del volumen de vista en el plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fd7b3-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7b3-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7b3-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd7b3-115">Alto del volumen de vista en el plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fd7b3-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fd7b3-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7b3-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd7b3-118">Valor Z del plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fd7b3-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fd7b3-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7b3-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd7b3-121">Valor Z del plano de vista lejana.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7b3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd7b3-122">Return value</span></span>

<span data-ttu-id="fd7b3-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd7b3-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd7b3-124">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva con la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7b3-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd7b3-125">Remarks</span></span>

<span data-ttu-id="fd7b3-126">Todos los parámetros de la **función D3DXMatrixPerspectiveRH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="fd7b3-127">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="fd7b3-128">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="fd7b3-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fd7b3-129">De este modo, la **función D3DXMatrixPerspectiveRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fd7b3-130">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="fd7b3-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="fd7b3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd7b3-131">Requirements</span></span>



| <span data-ttu-id="fd7b3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7b3-132">Requirement</span></span> | <span data-ttu-id="fd7b3-133">Value</span><span class="sxs-lookup"><span data-stu-id="fd7b3-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7b3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd7b3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fd7b3-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7b3-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd7b3-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd7b3-136">Library</span></span><br/> | <dl> <span data-ttu-id="fd7b3-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd7b3-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd7b3-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd7b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7b3-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fd7b3-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fd7b3-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="fd7b3-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="fd7b3-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="fd7b3-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="fd7b3-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="fd7b3-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
