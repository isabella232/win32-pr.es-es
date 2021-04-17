---
description: Gira un cuaternión sobre un eje arbitrario.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: Función D3DXQuaternionRotationAxis (D3DX10Math. h)
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
ms.openlocfilehash: 739f128ca1a56eed15ebc2528036875eaf2bb9b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718437"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="fba74-103">Función D3DXQuaternionRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fba74-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="fba74-104">Gira un cuaternión sobre un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="fba74-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba74-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba74-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="fba74-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba74-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fba74-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba74-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fba74-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fba74-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fba74-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fba74-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba74-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba74-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fba74-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fba74-112">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que identifica el eje sobre el que se va a girar el cuaternión.</span><span class="sxs-lookup"><span data-stu-id="fba74-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="fba74-113">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba74-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba74-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fba74-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fba74-115">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="fba74-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="fba74-116">Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="fba74-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba74-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba74-117">Return value</span></span>

<span data-ttu-id="fba74-118">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fba74-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fba74-119">Puntero a una estructura D3DXQUATERNION girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="fba74-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba74-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fba74-120">Remarks</span></span>

<span data-ttu-id="fba74-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fba74-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fba74-122">De esta manera, la función D3DXQuaternionRotationAxis se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="fba74-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fba74-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="fba74-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba74-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba74-124">Requirements</span></span>



| <span data-ttu-id="fba74-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba74-125">Requirement</span></span> | <span data-ttu-id="fba74-126">Value</span><span class="sxs-lookup"><span data-stu-id="fba74-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba74-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fba74-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fba74-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba74-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fba74-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fba74-129">Library</span></span><br/> | <dl> <span data-ttu-id="fba74-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba74-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fba74-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba74-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba74-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fba74-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
