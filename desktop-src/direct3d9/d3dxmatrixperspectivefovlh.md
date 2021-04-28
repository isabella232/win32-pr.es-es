---
description: 'Función D3DXMatrixPerspectiveFovLH (D3dx9math.h): crea una matriz de proyección de perspectiva de la izquierda basada en un campo de vista.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Función D3DXMatrixPerspectiveFovLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118353"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="18d49-103">Función D3DXMatrixPerspectiveFovLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="18d49-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="18d49-104">Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.</span><span class="sxs-lookup"><span data-stu-id="18d49-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18d49-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="18d49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18d49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d49-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18d49-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18d49-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="18d49-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18d49-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="18d49-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="18d49-110">*fovy* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="18d49-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d49-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18d49-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18d49-112">Campo de vista en la dirección y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="18d49-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="18d49-113">*Aspecto* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="18d49-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d49-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18d49-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18d49-115">Relación de aspecto, definida como ancho del espacio de vista dividido por alto.</span><span class="sxs-lookup"><span data-stu-id="18d49-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="18d49-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="18d49-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d49-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18d49-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18d49-118">Valor Z del plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="18d49-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="18d49-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="18d49-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d49-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18d49-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18d49-121">Valor Z del plano de vista lejana.</span><span class="sxs-lookup"><span data-stu-id="18d49-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d49-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18d49-122">Return value</span></span>

<span data-ttu-id="18d49-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="18d49-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="18d49-124">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva con la mano izquierda.</span><span class="sxs-lookup"><span data-stu-id="18d49-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="18d49-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18d49-125">Remarks</span></span>

<span data-ttu-id="18d49-126">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="18d49-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="18d49-127">De este modo, la función **D3DXMatrixPerspectiveFovLH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="18d49-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="18d49-128">Para cambiar el eje de relación de aspecto, use la fórmula de cálculo: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span><span class="sxs-lookup"><span data-stu-id="18d49-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="18d49-129">Como alternativa, agregue variables de relación de aspecto X e Y en la estructura para escalar el espacio de vista vertical: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="18d49-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="18d49-130">Esta función calcula la matriz devuelta como se muestra:</span><span class="sxs-lookup"><span data-stu-id="18d49-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="18d49-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18d49-131">Requirements</span></span>



| <span data-ttu-id="18d49-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d49-132">Requirement</span></span> | <span data-ttu-id="18d49-133">Value</span><span class="sxs-lookup"><span data-stu-id="18d49-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18d49-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18d49-134">Header</span></span><br/>  | <dl> <span data-ttu-id="18d49-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="18d49-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="18d49-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18d49-136">Library</span></span><br/> | <dl> <span data-ttu-id="18d49-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="18d49-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18d49-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18d49-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d49-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="18d49-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="18d49-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="18d49-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="18d49-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="18d49-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="18d49-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="18d49-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="18d49-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="18d49-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="18d49-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="18d49-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
