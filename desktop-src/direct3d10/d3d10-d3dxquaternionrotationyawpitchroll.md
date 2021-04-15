---
description: Crea un cuaternión con el guiñada, el tono y el rollo dados.
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Función D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d894be61f5f22322f83c4e4a6c6a724de4b9da4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708003"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="f1da9-103">Función D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f1da9-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="f1da9-104">Crea un cuaternión con el guiñada, el tono y el rollo dados.</span><span class="sxs-lookup"><span data-stu-id="f1da9-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1da9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1da9-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="f1da9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1da9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1da9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f1da9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1da9-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1da9-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f1da9-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f1da9-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1da9-110">*Guiñada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1da9-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1da9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1da9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1da9-112">Guiña alrededor del eje y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="f1da9-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f1da9-113">*Paso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1da9-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1da9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1da9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1da9-115">Paso alrededor del eje x, en radianes.</span><span class="sxs-lookup"><span data-stu-id="f1da9-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f1da9-116">Poner al *día* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1da9-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1da9-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1da9-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1da9-118">Desplazarse alrededor del eje z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="f1da9-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1da9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1da9-119">Return value</span></span>

<span data-ttu-id="f1da9-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1da9-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f1da9-121">Puntero a una estructura D3DXQUATERNION con el guiñada, el tono y el rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="f1da9-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1da9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1da9-122">Remarks</span></span>

<span data-ttu-id="f1da9-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f1da9-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f1da9-124">De esta manera, la función D3DXQuaternionRotationYawPitchRoll se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f1da9-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f1da9-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="f1da9-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1da9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1da9-126">Requirements</span></span>



| <span data-ttu-id="f1da9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1da9-127">Requirement</span></span> | <span data-ttu-id="f1da9-128">Value</span><span class="sxs-lookup"><span data-stu-id="f1da9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1da9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1da9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f1da9-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1da9-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f1da9-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1da9-131">Library</span></span><br/> | <dl> <span data-ttu-id="f1da9-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1da9-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1da9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1da9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1da9-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f1da9-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
