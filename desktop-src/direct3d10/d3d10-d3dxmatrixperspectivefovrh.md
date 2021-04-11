---
description: Crea una matriz de proyección de perspectiva a la derecha basada en un campo visual.
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Función D3DXMatrixPerspectiveFovRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: baad02b5840af8e244cd562def4aeb8f9ac2988a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003894"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="894f8-103">Función D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="894f8-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="894f8-104">Crea una matriz de proyección de perspectiva a la derecha basada en un campo visual.</span><span class="sxs-lookup"><span data-stu-id="894f8-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="894f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="894f8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="894f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="894f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894f8-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="894f8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="894f8-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="894f8-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="894f8-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="894f8-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="894f8-110">*fovy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="894f8-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894f8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="894f8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="894f8-112">Campo de vista en la dirección y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="894f8-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="894f8-113">*Aspecto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="894f8-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894f8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="894f8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="894f8-115">Relación de aspecto, definida como el ancho del espacio de la vista dividido por el alto.</span><span class="sxs-lookup"><span data-stu-id="894f8-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="894f8-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="894f8-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894f8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="894f8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="894f8-118">Valor Z del plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="894f8-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="894f8-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="894f8-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894f8-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="894f8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="894f8-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="894f8-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894f8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="894f8-122">Return value</span></span>

<span data-ttu-id="894f8-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="894f8-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="894f8-124">Puntero a una estructura D3DXMATRIX que es una matriz de proyección en perspectiva a la derecha.</span><span class="sxs-lookup"><span data-stu-id="894f8-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="894f8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="894f8-125">Remarks</span></span>

<span data-ttu-id="894f8-126">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="894f8-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="894f8-127">De esta manera, la función D3DXMatrixPerspectiveFovRH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="894f8-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="894f8-128">Esta función calcula la matriz devuelta como se muestra.</span><span class="sxs-lookup"><span data-stu-id="894f8-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="894f8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="894f8-129">Requirements</span></span>



| <span data-ttu-id="894f8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="894f8-130">Requirement</span></span> | <span data-ttu-id="894f8-131">Value</span><span class="sxs-lookup"><span data-stu-id="894f8-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="894f8-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="894f8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="894f8-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="894f8-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="894f8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="894f8-134">Library</span></span><br/> | <dl> <span data-ttu-id="894f8-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="894f8-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="894f8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="894f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894f8-137">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="894f8-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
