---
description: Crea una matriz con un guiñada, un tono y un rollo especificados.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Función D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003944"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="ad305-103">Función D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ad305-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="ad305-104">Crea una matriz con un guiñada, un tono y un rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="ad305-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad305-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad305-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="ad305-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad305-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad305-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad305-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad305-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad305-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ad305-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad305-110">*Guiñada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad305-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad305-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad305-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad305-112">Guiña alrededor del eje y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="ad305-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ad305-113">*Paso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad305-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad305-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad305-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad305-115">Paso alrededor del eje x, en radianes.</span><span class="sxs-lookup"><span data-stu-id="ad305-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ad305-116">Poner al *día* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad305-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad305-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad305-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad305-118">Desplazarse alrededor del eje z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="ad305-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad305-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad305-119">Return value</span></span>

<span data-ttu-id="ad305-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad305-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad305-121">Puntero a una estructura D3DXMATRIX con el guiñada, el tono y el rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="ad305-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad305-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad305-122">Remarks</span></span>

<span data-ttu-id="ad305-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ad305-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ad305-124">De esta manera, la función D3DXMatrixRotationYawPitchRoll se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="ad305-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ad305-125">El orden de las transformaciones se revierte primero, después por el paso y después por el guiñada.</span><span class="sxs-lookup"><span data-stu-id="ad305-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="ad305-126">En relación con el eje de coordenadas local del objeto, es equivalente a la rotación alrededor del eje z, seguido de la rotación alrededor del eje x, seguido de la rotación alrededor del eje y, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ad305-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Ilustración del rollo, el tono y el guiñada como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="ad305-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad305-128">Requirements</span></span>



| <span data-ttu-id="ad305-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad305-129">Requirement</span></span> | <span data-ttu-id="ad305-130">Value</span><span class="sxs-lookup"><span data-stu-id="ad305-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad305-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad305-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ad305-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad305-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ad305-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad305-133">Library</span></span><br/> | <dl> <span data-ttu-id="ad305-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad305-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad305-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad305-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad305-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="ad305-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
