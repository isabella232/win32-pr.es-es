---
description: 'Función D3DXMatrixRotationX (D3DX10Math.h): crea una matriz que gira alrededor del eje X.'
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: Función D3DXMatrixRotationX (D3DX10Math.h)
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
ms.openlocfilehash: 53c4bf27a359bd6d131f8d6d9c685e929d1a9ec1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108993"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="97c75-103">Función D3DXMatrixRotationX (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="97c75-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="97c75-104">Crea una matriz que gira alrededor del eje X.</span><span class="sxs-lookup"><span data-stu-id="97c75-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c75-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="97c75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c75-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97c75-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c75-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97c75-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97c75-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="97c75-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97c75-110">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="97c75-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c75-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c75-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c75-112">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="97c75-112">Angle of rotation in radians.</span></span> <span data-ttu-id="97c75-113">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="97c75-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c75-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97c75-114">Return value</span></span>

<span data-ttu-id="97c75-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97c75-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97c75-116">Puntero a una estructura D3DXMATRIX girada alrededor del eje X.</span><span class="sxs-lookup"><span data-stu-id="97c75-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c75-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97c75-117">Remarks</span></span>

<span data-ttu-id="97c75-118">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="97c75-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="97c75-119">De este modo, la función D3DXMatrixRotationX se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="97c75-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c75-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c75-120">Requirements</span></span>



| <span data-ttu-id="97c75-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c75-121">Requirement</span></span> | <span data-ttu-id="97c75-122">Value</span><span class="sxs-lookup"><span data-stu-id="97c75-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c75-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97c75-123">Header</span></span><br/>  | <dl> <span data-ttu-id="97c75-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="97c75-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="97c75-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97c75-125">Library</span></span><br/> | <dl> <span data-ttu-id="97c75-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c75-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97c75-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="97c75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c75-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="97c75-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
