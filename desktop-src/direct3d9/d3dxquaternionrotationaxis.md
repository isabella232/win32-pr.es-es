---
description: Gira un cuaternión sobre un eje arbitrario.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Función D3DXQuaternionRotationAxis (D3dx9math. h)
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
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707827"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="be3f3-103">Función D3DXQuaternionRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="be3f3-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="be3f3-104">Gira un cuaternión sobre un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="be3f3-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3f3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be3f3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="be3f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be3f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3f3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be3f3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be3f3-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="be3f3-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="be3f3-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="be3f3-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be3f3-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be3f3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3f3-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="be3f3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="be3f3-112">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que identifica el eje sobre el que se va a girar el cuaternión.</span><span class="sxs-lookup"><span data-stu-id="be3f3-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="be3f3-113">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be3f3-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3f3-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be3f3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be3f3-115">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="be3f3-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="be3f3-116">Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="be3f3-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3f3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be3f3-117">Return value</span></span>

<span data-ttu-id="be3f3-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="be3f3-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="be3f3-119">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="be3f3-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3f3-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be3f3-120">Remarks</span></span>

<span data-ttu-id="be3f3-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="be3f3-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="be3f3-122">De esta manera, la función **D3DXQuaternionRotationAxis** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="be3f3-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="be3f3-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="be3f3-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="be3f3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3f3-124">Requirements</span></span>



| <span data-ttu-id="be3f3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="be3f3-125">Requirement</span></span> | <span data-ttu-id="be3f3-126">Value</span><span class="sxs-lookup"><span data-stu-id="be3f3-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be3f3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be3f3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="be3f3-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be3f3-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="be3f3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be3f3-129">Library</span></span><br/> | <dl> <span data-ttu-id="be3f3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be3f3-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be3f3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="be3f3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3f3-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="be3f3-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="be3f3-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="be3f3-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="be3f3-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="be3f3-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
