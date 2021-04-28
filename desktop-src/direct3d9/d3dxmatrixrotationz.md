---
description: 'Función D3DXMatrixRotationZ (D3dx9math.h): crea una matriz que gira alrededor del eje Z.'
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: Función D3DXMatrixRotationZ (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b109f71052657a5d9c32d9af5cb38b2cbcf1f0e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118113"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="d18e1-103">Función D3DXMatrixRotationZ (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d18e1-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="d18e1-104">Crea una matriz que gira alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="d18e1-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d18e1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="d18e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d18e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18e1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d18e1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d18e1-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d18e1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d18e1-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d18e1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d18e1-110">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d18e1-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d18e1-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d18e1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d18e1-112">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="d18e1-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="d18e1-113">Los ángulos se miden en el sentido de las agujas del reloj cuando se ven desde el eje de rotación (lado positivo) hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="d18e1-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18e1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d18e1-114">Return value</span></span>

<span data-ttu-id="d18e1-115">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d18e1-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d18e1-116">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) girada alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="d18e1-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="d18e1-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d18e1-117">Remarks</span></span>

<span data-ttu-id="d18e1-118">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="d18e1-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d18e1-119">De este modo, la **función D3DXMatrixRotationZ** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="d18e1-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d18e1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18e1-120">Requirements</span></span>



| <span data-ttu-id="d18e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18e1-121">Requirement</span></span> | <span data-ttu-id="d18e1-122">Value</span><span class="sxs-lookup"><span data-stu-id="d18e1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d18e1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d18e1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d18e1-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d18e1-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d18e1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d18e1-125">Library</span></span><br/> | <dl> <span data-ttu-id="d18e1-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d18e1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d18e1-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d18e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18e1-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d18e1-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d18e1-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="d18e1-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="d18e1-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="d18e1-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="d18e1-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="d18e1-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="d18e1-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="d18e1-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="d18e1-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="d18e1-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
