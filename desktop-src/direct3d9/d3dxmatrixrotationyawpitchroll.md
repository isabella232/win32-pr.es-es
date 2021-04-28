---
description: 'Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h): crea una matriz con una yaw, pitch y roll especificada.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118153"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="718f7-103">Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="718f7-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="718f7-104">Crea una matriz con una yaw, pitch y roll especificada.</span><span class="sxs-lookup"><span data-stu-id="718f7-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="718f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="718f7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="718f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="718f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718f7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="718f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="718f7-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="718f7-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="718f7-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="718f7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="718f7-110">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="718f7-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718f7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="718f7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="718f7-112">Moverse alrededor del eje Y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="718f7-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="718f7-113">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="718f7-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718f7-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="718f7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="718f7-115">Inclinar alrededor del eje X, en radianes.</span><span class="sxs-lookup"><span data-stu-id="718f7-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="718f7-116">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="718f7-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718f7-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="718f7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="718f7-118">Revierte el eje Z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="718f7-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718f7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="718f7-119">Return value</span></span>

<span data-ttu-id="718f7-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="718f7-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="718f7-121">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) con el yaw, pitch y roll especificados.</span><span class="sxs-lookup"><span data-stu-id="718f7-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="718f7-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="718f7-122">Remarks</span></span>

<span data-ttu-id="718f7-123">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="718f7-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="718f7-124">De esta manera, la función **D3DXMatrixRotationYawPitchRoll** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="718f7-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="718f7-125">El orden de las transformaciones es roll first, then pitch, then yaw.</span><span class="sxs-lookup"><span data-stu-id="718f7-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="718f7-126">En relación con el eje de coordenadas local del objeto, esto equivale a la rotación alrededor del eje Z, seguida de la rotación alrededor del eje X, seguida de la rotación alrededor del eje Y, como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="718f7-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![ilustración de roll, pitch y yaw como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="718f7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="718f7-128">Requirements</span></span>



| <span data-ttu-id="718f7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="718f7-129">Requirement</span></span> | <span data-ttu-id="718f7-130">Value</span><span class="sxs-lookup"><span data-stu-id="718f7-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="718f7-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="718f7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="718f7-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="718f7-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="718f7-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="718f7-133">Library</span></span><br/> | <dl> <span data-ttu-id="718f7-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="718f7-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="718f7-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="718f7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718f7-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="718f7-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="718f7-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="718f7-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="718f7-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="718f7-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="718f7-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="718f7-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="718f7-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="718f7-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="718f7-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="718f7-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
