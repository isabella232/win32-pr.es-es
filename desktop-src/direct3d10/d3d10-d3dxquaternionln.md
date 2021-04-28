---
description: 'Función D3DXQuaternionLn (D3DX10Math.h): calcula el logaritmo natural.'
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Función D3DXQuaternionLn (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9abaaa231e424e55e496b7901882e9da17c59786
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103213"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="1905c-103">Función D3DXQuaternionLn (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1905c-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="1905c-104">Calcula el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="1905c-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="1905c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1905c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="1905c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1905c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1905c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1905c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1905c-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1905c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1905c-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1905c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1905c-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1905c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1905c-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1905c-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1905c-112">Puntero a la estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="1905c-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1905c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1905c-113">Return value</span></span>

<span data-ttu-id="1905c-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1905c-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1905c-115">Puntero a una estructura D3DXQUATERNION que es el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="1905c-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="1905c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1905c-116">Remarks</span></span>

<span data-ttu-id="1905c-117">La función D3DXQuaternionLn solo funciona para cuaterniones de unidad.</span><span class="sxs-lookup"><span data-stu-id="1905c-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="1905c-118">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1905c-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1905c-119">De esta manera, la función D3DXQuaternionLn se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="1905c-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1905c-120">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="1905c-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1905c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1905c-121">Requirements</span></span>



| <span data-ttu-id="1905c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1905c-122">Requirement</span></span> | <span data-ttu-id="1905c-123">Value</span><span class="sxs-lookup"><span data-stu-id="1905c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1905c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1905c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1905c-125"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1905c-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1905c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1905c-126">Library</span></span><br/> | <dl> <span data-ttu-id="1905c-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1905c-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1905c-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1905c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1905c-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1905c-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
