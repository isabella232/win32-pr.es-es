---
description: 'Función D3DXMatrixRotationZ (D3DX10Math.h): crea una matriz que gira alrededor del eje Z.'
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: Función D3DXMatrixRotationZ (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b952e310dd463d07a35fb294c4a50168361658a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108943"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="6a9bb-103">Función D3DXMatrixRotationZ (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="6a9bb-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="6a9bb-104">Crea una matriz que gira alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9bb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a9bb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="6a9bb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a9bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9bb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6a9bb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9bb-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a9bb-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a9bb-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a9bb-110">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6a9bb-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9bb-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a9bb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a9bb-112">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="6a9bb-113">Los ángulos se miden en el sentido de las agujas del reloj cuando se ven desde el eje de rotación (lado positivo) hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9bb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a9bb-114">Return value</span></span>

<span data-ttu-id="6a9bb-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a9bb-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a9bb-116">Puntero a una estructura D3DXMATRIX girada alrededor del eje Z.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a9bb-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a9bb-117">Remarks</span></span>

<span data-ttu-id="6a9bb-118">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6a9bb-119">De este modo, la función D3DXMatrixRotationZ se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9bb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a9bb-120">Requirements</span></span>



| <span data-ttu-id="6a9bb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9bb-121">Requirement</span></span> | <span data-ttu-id="6a9bb-122">Value</span><span class="sxs-lookup"><span data-stu-id="6a9bb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9bb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a9bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6a9bb-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9bb-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a9bb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a9bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="6a9bb-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a9bb-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a9bb-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6a9bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9bb-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6a9bb-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
