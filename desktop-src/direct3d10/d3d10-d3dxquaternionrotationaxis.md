---
description: 'Función D3DXQuaternionRotationAxis (D3DX10Math.h): gira un cuaternión sobre un eje arbitrario.'
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: Función D3DXQuaternionRotationAxis (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108773"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="93545-103">Función D3DXQuaternionRotationAxis (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="93545-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="93545-104">Gira un cuaternión sobre un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="93545-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="93545-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93545-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="93545-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93545-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="93545-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93545-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="93545-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="93545-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="93545-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93545-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="93545-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93545-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93545-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93545-112">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que identifica el eje sobre el que se va a girar el cuaternión.</span><span class="sxs-lookup"><span data-stu-id="93545-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="93545-113">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="93545-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93545-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93545-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93545-115">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="93545-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="93545-116">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="93545-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93545-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93545-117">Return value</span></span>

<span data-ttu-id="93545-118">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="93545-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="93545-119">Puntero a una estructura D3DXQUATERNION girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="93545-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="93545-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93545-120">Remarks</span></span>

<span data-ttu-id="93545-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="93545-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="93545-122">De este modo, la función D3DXQuaternionRotationAxis se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="93545-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="93545-123">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="93545-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="93545-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93545-124">Requirements</span></span>



| <span data-ttu-id="93545-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93545-125">Requirement</span></span> | <span data-ttu-id="93545-126">Value</span><span class="sxs-lookup"><span data-stu-id="93545-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93545-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93545-127">Header</span></span><br/>  | <dl> <span data-ttu-id="93545-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="93545-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="93545-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93545-129">Library</span></span><br/> | <dl> <span data-ttu-id="93545-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="93545-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93545-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="93545-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93545-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="93545-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
