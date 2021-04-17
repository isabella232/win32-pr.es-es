---
description: Calcula el logaritmo natural.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Función D3DXQuaternionLn (D3dx9math. h)
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
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548046"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="da0ed-103">Función D3DXQuaternionLn (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="da0ed-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="da0ed-104">Calcula el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="da0ed-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da0ed-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="da0ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da0ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0ed-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da0ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da0ed-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="da0ed-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da0ed-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="da0ed-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da0ed-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da0ed-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0ed-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="da0ed-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da0ed-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="da0ed-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da0ed-113">Return value</span></span>

<span data-ttu-id="da0ed-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="da0ed-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da0ed-115">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="da0ed-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0ed-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da0ed-116">Remarks</span></span>

<span data-ttu-id="da0ed-117">La función **D3DXQuaternionLn** solo funciona para los cuaterniones de unidad.</span><span class="sxs-lookup"><span data-stu-id="da0ed-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="da0ed-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="da0ed-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="da0ed-119">De esta manera, la función **D3DXQuaternionLn** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="da0ed-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="da0ed-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="da0ed-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0ed-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da0ed-121">Requirements</span></span>



| <span data-ttu-id="da0ed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="da0ed-122">Requirement</span></span> | <span data-ttu-id="da0ed-123">Value</span><span class="sxs-lookup"><span data-stu-id="da0ed-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0ed-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da0ed-124">Header</span></span><br/>  | <dl> <span data-ttu-id="da0ed-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0ed-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="da0ed-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da0ed-126">Library</span></span><br/> | <dl> <span data-ttu-id="da0ed-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da0ed-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da0ed-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="da0ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0ed-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="da0ed-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="da0ed-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="da0ed-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="da0ed-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="da0ed-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




