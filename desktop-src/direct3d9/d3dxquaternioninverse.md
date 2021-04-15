---
description: Conjuga y vuelve a normalizar un cuaternión.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: Función D3DXQuaternionInverse (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424484"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="0deb3-103">Función D3DXQuaternionInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0deb3-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="0deb3-104">Conjuga y vuelve a normalizar un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="0deb3-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="0deb3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0deb3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="0deb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0deb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0deb3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0deb3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0deb3-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0deb3-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0deb3-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="0deb3-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0deb3-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0deb3-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0deb3-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0deb3-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0deb3-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="0deb3-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0deb3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0deb3-113">Return value</span></span>

<span data-ttu-id="0deb3-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0deb3-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0deb3-115">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el cuaternión inverso del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="0deb3-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="0deb3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0deb3-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="0deb3-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="0deb3-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0deb3-118">De esta manera, la función **D3DXQuaternionInverse** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="0deb3-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0deb3-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="0deb3-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0deb3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0deb3-120">Requirements</span></span>



| <span data-ttu-id="0deb3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0deb3-121">Requirement</span></span> | <span data-ttu-id="0deb3-122">Value</span><span class="sxs-lookup"><span data-stu-id="0deb3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0deb3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0deb3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0deb3-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0deb3-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0deb3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0deb3-125">Library</span></span><br/> | <dl> <span data-ttu-id="0deb3-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0deb3-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0deb3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0deb3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0deb3-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0deb3-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0deb3-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="0deb3-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="0deb3-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="0deb3-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




