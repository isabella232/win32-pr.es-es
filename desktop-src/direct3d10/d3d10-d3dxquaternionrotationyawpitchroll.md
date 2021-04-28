---
description: 'Función D3DXQuaternionRotationYawPitchRoll (D3DX10Math.h): crea un cuaternión con el yaw, pitch y roll dados.'
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Función D3DXQuaternionRotationYawPitchRoll (D3DX10Math.h)
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
ms.openlocfilehash: cefcf9a927cee0d8f7c83ff42ae6ca4fc699bb09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108753"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="8ba4c-103">Función D3DXQuaternionRotationYawPitchRoll (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8ba4c-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="8ba4c-104">Crea un cuaternión con el guión, el lanzamiento y el lanzamiento dados.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba4c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba4c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="8ba4c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ba4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba4c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ba4c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba4c-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba4c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8ba4c-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ba4c-110">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8ba4c-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba4c-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba4c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba4c-112">Eje Y alrededor del eje Y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8ba4c-113">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8ba4c-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba4c-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba4c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba4c-115">Inclinar alrededor del eje X, en radianes.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8ba4c-116">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8ba4c-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba4c-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba4c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba4c-118">Revierte el eje Z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba4c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ba4c-119">Return value</span></span>

<span data-ttu-id="8ba4c-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba4c-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8ba4c-121">Puntero a una estructura D3DXQUATERNION con el guión, el paso y el lanzamiento especificados.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba4c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ba4c-122">Remarks</span></span>

<span data-ttu-id="8ba4c-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8ba4c-124">De este modo, la función D3DXQuaternionRotationYawPitchRoll se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8ba4c-125">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="8ba4c-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba4c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba4c-126">Requirements</span></span>



| <span data-ttu-id="8ba4c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba4c-127">Requirement</span></span> | <span data-ttu-id="8ba4c-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ba4c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba4c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ba4c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba4c-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba4c-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8ba4c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ba4c-131">Library</span></span><br/> | <dl> <span data-ttu-id="8ba4c-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba4c-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ba4c-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ba4c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba4c-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8ba4c-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
