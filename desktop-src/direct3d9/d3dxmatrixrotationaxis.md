---
description: 'Función D3DXMatrixRotationAxis (D3dx9math.h): crea una matriz que gira alrededor de un eje arbitrario.'
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: Función D3DXMatrixRotationAxis (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118193"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="a30f1-103">Función D3DXMatrixRotationAxis (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a30f1-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="a30f1-104">Crea una matriz que gira alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a30f1-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a30f1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="a30f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a30f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30f1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a30f1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a30f1-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a30f1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a30f1-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a30f1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a30f1-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a30f1-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30f1-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a30f1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a30f1-112">Puntero al eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a30f1-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="a30f1-113">Vea [**D3DXVECTOR3.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="a30f1-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="a30f1-114">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a30f1-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30f1-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a30f1-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a30f1-116">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="a30f1-116">Angle of rotation in radians.</span></span> <span data-ttu-id="a30f1-117">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="a30f1-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30f1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30f1-118">Return value</span></span>

<span data-ttu-id="a30f1-119">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a30f1-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a30f1-120">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="a30f1-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="a30f1-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a30f1-121">Remarks</span></span>

<span data-ttu-id="a30f1-122">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="a30f1-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a30f1-123">De este modo, la **función D3DXMatrixRotationAxis** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="a30f1-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30f1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30f1-124">Requirements</span></span>



| <span data-ttu-id="a30f1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30f1-125">Requirement</span></span> | <span data-ttu-id="a30f1-126">Value</span><span class="sxs-lookup"><span data-stu-id="a30f1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a30f1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a30f1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a30f1-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a30f1-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a30f1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a30f1-129">Library</span></span><br/> | <dl> <span data-ttu-id="a30f1-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a30f1-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a30f1-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a30f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30f1-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a30f1-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a30f1-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="a30f1-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="a30f1-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="a30f1-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="a30f1-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="a30f1-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="a30f1-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a30f1-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="a30f1-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="a30f1-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
