---
description: 'Función D3DXQuaternionSlerp (D3dx9math.h): interpola entre dos cuaterniones, mediante interpolación lineal esférica.'
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Función D3DXQuaternionSlerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb9110da7fae4ebbf4609d361124dbbcdedfe59b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093943"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="244ab-103">Función D3DXQuaternionSlerp (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="244ab-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="244ab-104">Interpola entre dos cuaterniones mediante la interpolación lineal esférica.</span><span class="sxs-lookup"><span data-stu-id="244ab-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="244ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="244ab-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="244ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="244ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244ab-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="244ab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="244ab-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="244ab-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="244ab-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="244ab-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="244ab-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="244ab-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="244ab-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="244ab-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="244ab-112">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="244ab-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="244ab-113">*pQ2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="244ab-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="244ab-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="244ab-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="244ab-115">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="244ab-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="244ab-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="244ab-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="244ab-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="244ab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="244ab-118">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="244ab-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244ab-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="244ab-119">Return value</span></span>

<span data-ttu-id="244ab-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="244ab-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="244ab-121">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la interpolación.</span><span class="sxs-lookup"><span data-stu-id="244ab-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="244ab-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="244ab-122">Remarks</span></span>

<span data-ttu-id="244ab-123">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="244ab-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="244ab-124">De este modo, la **función D3DXQuaternionSlerp** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="244ab-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="244ab-125">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="244ab-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="244ab-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="244ab-126">Requirements</span></span>



| <span data-ttu-id="244ab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="244ab-127">Requirement</span></span> | <span data-ttu-id="244ab-128">Value</span><span class="sxs-lookup"><span data-stu-id="244ab-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="244ab-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="244ab-129">Header</span></span><br/>  | <dl> <span data-ttu-id="244ab-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="244ab-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="244ab-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="244ab-131">Library</span></span><br/> | <dl> <span data-ttu-id="244ab-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="244ab-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="244ab-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="244ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244ab-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="244ab-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
