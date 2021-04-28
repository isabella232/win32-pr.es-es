---
description: 'Función D3DXMatrixPerspectiveFovRH (D3dx9math.h): crea una matriz de proyección de perspectiva con la derecha basada en un campo de vista.'
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Función D3DXMatrixPerspectiveFovRH (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8860a5d9fed13e8acdedfe67ed94a97911a6de0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118333"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="c75b4-103">Función D3DXMatrixPerspectiveFovRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c75b4-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="c75b4-104">Crea una matriz de proyección de perspectiva a la derecha basada en un campo visual.</span><span class="sxs-lookup"><span data-stu-id="c75b4-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c75b4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c75b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c75b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75b4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c75b4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b4-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c75b4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c75b4-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c75b4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c75b4-110">*fovy* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c75b4-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c75b4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c75b4-112">Campo de vista en la dirección y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="c75b4-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="c75b4-113">*Aspecto* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c75b4-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b4-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c75b4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c75b4-115">Relación de aspecto, definida como ancho del espacio de vista dividido por alto.</span><span class="sxs-lookup"><span data-stu-id="c75b4-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="c75b4-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c75b4-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b4-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c75b4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c75b4-118">Valor Z del plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="c75b4-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c75b4-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c75b4-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b4-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c75b4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c75b4-121">Valor Z del plano de vista lejana.</span><span class="sxs-lookup"><span data-stu-id="c75b4-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75b4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c75b4-122">Return value</span></span>

<span data-ttu-id="c75b4-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c75b4-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c75b4-124">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva con la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="c75b4-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75b4-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c75b4-125">Remarks</span></span>

<span data-ttu-id="c75b4-126">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="c75b4-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c75b4-127">De este modo, la función **D3DXMatrixPerspectiveFovRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c75b4-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c75b4-128">Para cambiar el eje de relación de aspecto, use la fórmula de cálculo: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span><span class="sxs-lookup"><span data-stu-id="c75b4-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="c75b4-129">Como alternativa, agregue variables de relación de aspecto X e Y en la estructura para escalar el espacio de vista vertical: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="c75b4-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="c75b4-130">Esta función calcula la matriz devuelta como se muestra.</span><span class="sxs-lookup"><span data-stu-id="c75b4-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="c75b4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c75b4-131">Requirements</span></span>



| <span data-ttu-id="c75b4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c75b4-132">Requirement</span></span> | <span data-ttu-id="c75b4-133">Value</span><span class="sxs-lookup"><span data-stu-id="c75b4-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c75b4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c75b4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c75b4-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c75b4-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c75b4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c75b4-136">Library</span></span><br/> | <dl> <span data-ttu-id="c75b4-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c75b4-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c75b4-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c75b4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75b4-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c75b4-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c75b4-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="c75b4-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="c75b4-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c75b4-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="c75b4-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c75b4-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="c75b4-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c75b4-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="c75b4-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c75b4-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
