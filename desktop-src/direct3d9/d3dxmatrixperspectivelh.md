---
description: Crea una matriz de proyección de perspectiva izquierda
ms.assetid: 07bbbca8-ad1e-4177-97d4-601b33179b47
title: Función D3DXMatrixPerspectiveLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf7e6a446202a86e126b2cea0c4a09f19bf6ffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718393"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="1c660-103">Función D3DXMatrixPerspectiveLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1c660-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="1c660-104">Crea una matriz de proyección de perspectiva izquierda</span><span class="sxs-lookup"><span data-stu-id="1c660-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="1c660-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c660-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1c660-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c660-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1c660-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c660-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c660-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1c660-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1c660-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1c660-110">*w* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1c660-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c660-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c660-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c660-112">Ancho del volumen de vista en el plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="1c660-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1c660-113">*h* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1c660-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c660-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c660-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c660-115">Alto del volumen de vista en el plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="1c660-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1c660-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c660-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c660-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c660-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c660-118">Valor Z del plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="1c660-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1c660-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c660-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c660-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c660-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c660-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="1c660-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c660-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c660-122">Return value</span></span>

<span data-ttu-id="1c660-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c660-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1c660-124">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva izquierda.</span><span class="sxs-lookup"><span data-stu-id="1c660-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c660-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c660-125">Remarks</span></span>

<span data-ttu-id="1c660-126">Todos los parámetros de la función **D3DXMatrixPerspectiveLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="1c660-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="1c660-127">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="1c660-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1c660-128">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="1c660-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1c660-129">De esta manera, la función **D3DXMatrixPerspectiveLH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="1c660-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1c660-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="1c660-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="1c660-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c660-131">Requirements</span></span>



| <span data-ttu-id="1c660-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c660-132">Requirement</span></span> | <span data-ttu-id="1c660-133">Value</span><span class="sxs-lookup"><span data-stu-id="1c660-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c660-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c660-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1c660-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c660-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1c660-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c660-136">Library</span></span><br/> | <dl> <span data-ttu-id="1c660-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c660-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c660-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c660-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c660-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1c660-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1c660-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="1c660-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="1c660-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="1c660-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="1c660-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="1c660-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="1c660-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="1c660-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="1c660-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="1c660-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
