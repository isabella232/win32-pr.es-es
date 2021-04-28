---
description: 'Función D3DXMatrixRotationY (D3dx9math.h): crea una matriz que gira alrededor del eje Y.'
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: Función D3DXMatrixRotationY (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 902325890b02416e796940388bca7a6548773be5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118133"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="136ba-103">Función D3DXMatrixRotationY (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="136ba-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="136ba-104">Crea una matriz que gira alrededor del eje Y.</span><span class="sxs-lookup"><span data-stu-id="136ba-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="136ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="136ba-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="136ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="136ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="136ba-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="136ba-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="136ba-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="136ba-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="136ba-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="136ba-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-110">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="136ba-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="136ba-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="136ba-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="136ba-112">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="136ba-112">Angle of rotation in radians.</span></span> <span data-ttu-id="136ba-113">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="136ba-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="136ba-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="136ba-114">Return value</span></span>

<span data-ttu-id="136ba-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="136ba-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="136ba-116">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) girada alrededor del eje Y.</span><span class="sxs-lookup"><span data-stu-id="136ba-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="136ba-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="136ba-117">Remarks</span></span>

<span data-ttu-id="136ba-118">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="136ba-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="136ba-119">De esta manera, la **función D3DXMatrixRotationY** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="136ba-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="136ba-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136ba-120">Requirements</span></span>



| <span data-ttu-id="136ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="136ba-121">Requirement</span></span> | <span data-ttu-id="136ba-122">Value</span><span class="sxs-lookup"><span data-stu-id="136ba-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="136ba-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="136ba-123">Header</span></span><br/>  | <dl> <span data-ttu-id="136ba-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="136ba-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="136ba-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="136ba-125">Library</span></span><br/> | <dl> <span data-ttu-id="136ba-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="136ba-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="136ba-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="136ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136ba-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="136ba-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="136ba-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="136ba-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="136ba-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="136ba-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="136ba-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="136ba-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="136ba-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="136ba-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="136ba-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="136ba-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
