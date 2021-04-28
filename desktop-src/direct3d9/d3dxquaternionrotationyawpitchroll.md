---
description: 'Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h): crea un cuaternión con el yaw, pitch y roll dados.'
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118003"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="525c4-103">Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="525c4-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="525c4-104">Crea un cuaternión con el guión, el lanzamiento y el lanzamiento dados.</span><span class="sxs-lookup"><span data-stu-id="525c4-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="525c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="525c4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="525c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="525c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="525c4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="525c4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="525c4-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="525c4-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="525c4-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="525c4-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="525c4-110">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="525c4-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="525c4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="525c4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="525c4-112">Eje Y alrededor del eje Y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="525c4-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="525c4-113">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="525c4-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="525c4-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="525c4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="525c4-115">Inclinar alrededor del eje X, en radianes.</span><span class="sxs-lookup"><span data-stu-id="525c4-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="525c4-116">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="525c4-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="525c4-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="525c4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="525c4-118">Revierte el eje Z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="525c4-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="525c4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="525c4-119">Return value</span></span>

<span data-ttu-id="525c4-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="525c4-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="525c4-121">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) con el guión, el paso y el lanzamiento especificados.</span><span class="sxs-lookup"><span data-stu-id="525c4-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="525c4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="525c4-122">Remarks</span></span>

<span data-ttu-id="525c4-123">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="525c4-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="525c4-124">De este modo, la función **D3DXQuaternionRotationYawPitchRoll** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="525c4-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="525c4-125">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="525c4-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="525c4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="525c4-126">Requirements</span></span>



| <span data-ttu-id="525c4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="525c4-127">Requirement</span></span> | <span data-ttu-id="525c4-128">Value</span><span class="sxs-lookup"><span data-stu-id="525c4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="525c4-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="525c4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="525c4-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="525c4-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="525c4-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="525c4-131">Library</span></span><br/> | <dl> <span data-ttu-id="525c4-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="525c4-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="525c4-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="525c4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="525c4-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="525c4-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="525c4-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="525c4-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="525c4-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="525c4-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
