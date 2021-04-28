---
description: 'Función D3DXQuaternionRotationAxis (D3dx9math.h): gira un cuaternión sobre un eje arbitrario.'
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Función D3DXQuaternionRotationAxis (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5cbbdc3603b5e2eb7a03f592d44fa88f07ef015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118023"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="34cec-103">Función D3DXQuaternionRotationAxis (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="34cec-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="34cec-104">Gira un cuaternión sobre un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="34cec-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34cec-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="34cec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34cec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34cec-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34cec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34cec-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="34cec-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="34cec-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="34cec-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34cec-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="34cec-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34cec-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="34cec-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="34cec-112">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que identifica el eje sobre el que se va a girar el cuaternión.</span><span class="sxs-lookup"><span data-stu-id="34cec-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="34cec-113">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="34cec-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34cec-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34cec-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34cec-115">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="34cec-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="34cec-116">Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="34cec-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34cec-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34cec-117">Return value</span></span>

<span data-ttu-id="34cec-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="34cec-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="34cec-119">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="34cec-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="34cec-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34cec-120">Remarks</span></span>

<span data-ttu-id="34cec-121">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="34cec-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="34cec-122">De este modo, la **función D3DXQuaternionRotationAxis** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="34cec-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="34cec-123">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="34cec-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="34cec-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34cec-124">Requirements</span></span>



| <span data-ttu-id="34cec-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="34cec-125">Requirement</span></span> | <span data-ttu-id="34cec-126">Value</span><span class="sxs-lookup"><span data-stu-id="34cec-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34cec-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34cec-127">Header</span></span><br/>  | <dl> <span data-ttu-id="34cec-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="34cec-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="34cec-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34cec-129">Library</span></span><br/> | <dl> <span data-ttu-id="34cec-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="34cec-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34cec-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34cec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34cec-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="34cec-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="34cec-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="34cec-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="34cec-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="34cec-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
