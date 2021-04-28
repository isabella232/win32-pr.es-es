---
description: 'Función D3DXQuaternionSquad (D3DX10Math.h): interpola entre cuaterniones, mediante la interpolación de cuadrángulo esférico.'
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Función D3DXQuaternionSquad (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108763"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="d6bf6-103">Función D3DXQuaternionSquad (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d6bf6-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="d6bf6-104">Interpola entre cuaterniones mediante la interpolación de cuadrángulo esférica.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bf6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6bf6-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="d6bf6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6bf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bf6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf6-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-112">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf6-113">*pA* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-115">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf6-116">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-118">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf6-119">*pC* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-121">Puntero a una estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf6-122">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bf6-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6bf6-124">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bf6-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6bf6-125">Return value</span></span>

<span data-ttu-id="d6bf6-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6bf6-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d6bf6-127">Puntero a una estructura D3DXQUATERNION que es el resultado de la interpolación esférica de cuadrángulo.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6bf6-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6bf6-128">Remarks</span></span>

<span data-ttu-id="d6bf6-129">Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:</span><span class="sxs-lookup"><span data-stu-id="d6bf6-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="d6bf6-130">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d6bf6-131">De esta manera, la función D3DXQuaternionSquad se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d6bf6-132">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6bf6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6bf6-133">Requirements</span></span>



| <span data-ttu-id="d6bf6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6bf6-134">Requirement</span></span> | <span data-ttu-id="d6bf6-135">Value</span><span class="sxs-lookup"><span data-stu-id="d6bf6-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bf6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6bf6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d6bf6-137"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf6-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d6bf6-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6bf6-138">Library</span></span><br/> | <dl> <span data-ttu-id="d6bf6-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf6-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6bf6-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6bf6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bf6-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d6bf6-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
