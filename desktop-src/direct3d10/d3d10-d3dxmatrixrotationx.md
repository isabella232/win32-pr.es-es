---
description: Crea una matriz que gira alrededor del eje x.
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: Función D3DXMatrixRotationX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5eade695a3b410877665557bd42d61d1d89b18e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698360"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="e7b1f-103">Función D3DXMatrixRotationX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e7b1f-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="e7b1f-104">Crea una matriz que gira alrededor del eje x.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b1f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7b1f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e7b1f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b1f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e7b1f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b1f-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b1f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7b1f-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e7b1f-110">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7b1f-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b1f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b1f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7b1f-112">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-112">Angle of rotation in radians.</span></span> <span data-ttu-id="e7b1f-113">Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b1f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7b1f-114">Return value</span></span>

<span data-ttu-id="e7b1f-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b1f-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7b1f-116">Puntero a una estructura D3DXMATRIX girada alrededor del eje x.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b1f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b1f-117">Remarks</span></span>

<span data-ttu-id="e7b1f-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e7b1f-119">De esta manera, la función D3DXMatrixRotationX se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b1f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b1f-120">Requirements</span></span>



| <span data-ttu-id="e7b1f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b1f-121">Requirement</span></span> | <span data-ttu-id="e7b1f-122">Value</span><span class="sxs-lookup"><span data-stu-id="e7b1f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b1f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b1f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b1f-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b1f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b1f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7b1f-125">Library</span></span><br/> | <dl> <span data-ttu-id="e7b1f-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7b1f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7b1f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b1f-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e7b1f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
