---
description: 'Función D3DXQuaternionLn (D3dx9math.h): calcula el logaritmo natural.'
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Función D3DXQuaternionLn (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094063"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="e1c58-103">Función D3DXQuaternionLn (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e1c58-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="e1c58-104">Calcula el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="e1c58-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1c58-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="e1c58-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1c58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c58-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e1c58-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c58-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1c58-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e1c58-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e1c58-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e1c58-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e1c58-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c58-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1c58-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e1c58-112">Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e1c58-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c58-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1c58-113">Return value</span></span>

<span data-ttu-id="e1c58-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1c58-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e1c58-115">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="e1c58-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c58-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1c58-116">Remarks</span></span>

<span data-ttu-id="e1c58-117">La **función D3DXQuaternionLn** solo funciona para cuaterniones de unidad.</span><span class="sxs-lookup"><span data-stu-id="e1c58-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="e1c58-118">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="e1c58-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e1c58-119">De esta manera, la **función D3DXQuaternionLn** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e1c58-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e1c58-120">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="e1c58-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c58-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c58-121">Requirements</span></span>



| <span data-ttu-id="e1c58-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1c58-122">Requirement</span></span> | <span data-ttu-id="e1c58-123">Value</span><span class="sxs-lookup"><span data-stu-id="e1c58-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c58-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1c58-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e1c58-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e1c58-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1c58-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1c58-126">Library</span></span><br/> | <dl> <span data-ttu-id="e1c58-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1c58-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1c58-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1c58-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c58-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e1c58-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e1c58-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="e1c58-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="e1c58-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="e1c58-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




