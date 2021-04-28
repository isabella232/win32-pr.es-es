---
description: 'Función D3DXMatrixRotationAxis (D3DX10Math.h): crea una matriz que gira alrededor de un eje arbitrario.'
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Función D3DXMatrixRotationAxis (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ea5b8b0a40e876af454daa8915c0e455d691d08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109003"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="e98a4-103">Función D3DXMatrixRotationAxis (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="e98a4-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="e98a4-104">Crea una matriz que gira alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e98a4-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e98a4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e98a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e98a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98a4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e98a4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98a4-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e98a4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e98a4-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e98a4-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e98a4-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e98a4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e98a4-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e98a4-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e98a4-112">Puntero al eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e98a4-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="e98a4-113">Vea [**D3DXVECTOR3.**](d3d10-d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="e98a4-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="e98a4-114">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e98a4-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e98a4-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e98a4-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e98a4-116">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="e98a4-116">Angle of rotation in radians.</span></span> <span data-ttu-id="e98a4-117">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="e98a4-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98a4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e98a4-118">Return value</span></span>

<span data-ttu-id="e98a4-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e98a4-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e98a4-120">Puntero a una estructura D3DXMATRIX girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="e98a4-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98a4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e98a4-121">Remarks</span></span>

<span data-ttu-id="e98a4-122">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e98a4-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e98a4-123">De este modo, la función D3DXMatrixRotationAxis se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e98a4-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98a4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e98a4-124">Requirements</span></span>



| <span data-ttu-id="e98a4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e98a4-125">Requirement</span></span> | <span data-ttu-id="e98a4-126">Value</span><span class="sxs-lookup"><span data-stu-id="e98a4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e98a4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e98a4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e98a4-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e98a4-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e98a4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e98a4-129">Library</span></span><br/> | <dl> <span data-ttu-id="e98a4-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e98a4-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e98a4-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e98a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98a4-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e98a4-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
