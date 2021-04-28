---
description: 'Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h): crea una matriz con una yaw, pitch y roll especificada.'
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)
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
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108953"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="62225-103">Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="62225-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="62225-104">Crea una matriz con una yaw, pitch y roll especificada.</span><span class="sxs-lookup"><span data-stu-id="62225-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="62225-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62225-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="62225-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62225-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62225-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62225-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="62225-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="62225-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="62225-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="62225-110">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="62225-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62225-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62225-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62225-112">Moverse alrededor del eje Y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="62225-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="62225-113">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="62225-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62225-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62225-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62225-115">Inclinar alrededor del eje X, en radianes.</span><span class="sxs-lookup"><span data-stu-id="62225-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="62225-116">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="62225-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62225-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62225-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62225-118">Revierte el eje Z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="62225-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62225-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62225-119">Return value</span></span>

<span data-ttu-id="62225-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="62225-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="62225-121">Puntero a una estructura D3DXMATRIX con el yaw, pitch y roll especificados.</span><span class="sxs-lookup"><span data-stu-id="62225-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="62225-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62225-122">Remarks</span></span>

<span data-ttu-id="62225-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="62225-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="62225-124">De esta manera, la función D3DXMatrixRotationYawPitchRoll se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="62225-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="62225-125">El orden de las transformaciones es roll first, then pitch, then yaw.</span><span class="sxs-lookup"><span data-stu-id="62225-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="62225-126">En relación con el eje de coordenadas local del objeto, esto equivale a la rotación alrededor del eje Z, seguida de la rotación alrededor del eje X, seguida de la rotación alrededor del eje Y, como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="62225-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![ilustración de roll, pitch y yaw como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="62225-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62225-128">Requirements</span></span>



| <span data-ttu-id="62225-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="62225-129">Requirement</span></span> | <span data-ttu-id="62225-130">Value</span><span class="sxs-lookup"><span data-stu-id="62225-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62225-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62225-131">Header</span></span><br/>  | <dl> <span data-ttu-id="62225-132"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="62225-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="62225-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62225-133">Library</span></span><br/> | <dl> <span data-ttu-id="62225-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="62225-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62225-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62225-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62225-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="62225-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
