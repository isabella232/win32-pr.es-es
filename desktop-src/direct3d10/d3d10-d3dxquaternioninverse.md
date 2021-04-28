---
description: 'Función D3DXQuaternionInverse (D3DX10Math.h): conjuga y anula un cuaternión.'
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: Función D3DXQuaternionInverse (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103203"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="934ed-103">Función D3DXQuaternionInverse (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="934ed-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="934ed-104">Conjuga y reemita un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="934ed-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="934ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="934ed-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="934ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="934ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934ed-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="934ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="934ed-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="934ed-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="934ed-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="934ed-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="934ed-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="934ed-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934ed-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="934ed-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="934ed-112">Puntero a la estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="934ed-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="934ed-113">Return value</span></span>

<span data-ttu-id="934ed-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="934ed-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="934ed-115">Puntero a una estructura D3DXQUATERNION que es el cuaternión inverso del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="934ed-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="934ed-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="934ed-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="934ed-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="934ed-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="934ed-118">De esta manera, la función D3DXQuaternionInverse se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="934ed-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="934ed-119">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="934ed-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="934ed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="934ed-120">Requirements</span></span>



| <span data-ttu-id="934ed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="934ed-121">Requirement</span></span> | <span data-ttu-id="934ed-122">Value</span><span class="sxs-lookup"><span data-stu-id="934ed-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="934ed-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="934ed-123">Header</span></span><br/>  | <dl> <span data-ttu-id="934ed-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="934ed-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="934ed-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="934ed-125">Library</span></span><br/> | <dl> <span data-ttu-id="934ed-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="934ed-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="934ed-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="934ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934ed-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="934ed-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
