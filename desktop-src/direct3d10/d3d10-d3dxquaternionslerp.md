---
description: 'Función D3DXQuaternionSlerp (D3DX10Math.h): interpola entre dos cuaterniones mediante la interpolación lineal esférica.'
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Función D3DXQuaternionSlerp (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103123"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="f65a5-103">Función D3DXQuaternionSlerp (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f65a5-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="f65a5-104">Interpola entre dos cuaterniones mediante la interpolación lineal esférica.</span><span class="sxs-lookup"><span data-stu-id="f65a5-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f65a5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="f65a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f65a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65a5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f65a5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f65a5-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f65a5-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f65a5-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f65a5-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f65a5-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f65a5-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65a5-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f65a5-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f65a5-112">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="f65a5-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f65a5-113">*pQ2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f65a5-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65a5-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f65a5-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f65a5-115">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="f65a5-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f65a5-116">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f65a5-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65a5-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f65a5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f65a5-118">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="f65a5-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65a5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f65a5-119">Return value</span></span>

<span data-ttu-id="f65a5-120">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f65a5-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f65a5-121">Puntero a una estructura D3DXQUATERNION que es el resultado de la interpolación.</span><span class="sxs-lookup"><span data-stu-id="f65a5-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f65a5-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f65a5-122">Remarks</span></span>

<span data-ttu-id="f65a5-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f65a5-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f65a5-124">De este modo, la función D3DXQuaternionSlerp se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="f65a5-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f65a5-125">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="f65a5-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f65a5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f65a5-126">Requirements</span></span>



| <span data-ttu-id="f65a5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65a5-127">Requirement</span></span> | <span data-ttu-id="f65a5-128">Value</span><span class="sxs-lookup"><span data-stu-id="f65a5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f65a5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f65a5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f65a5-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f65a5-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f65a5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f65a5-131">Library</span></span><br/> | <dl> <span data-ttu-id="f65a5-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f65a5-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f65a5-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f65a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65a5-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f65a5-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
