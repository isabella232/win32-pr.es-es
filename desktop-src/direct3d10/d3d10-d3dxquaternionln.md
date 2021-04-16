---
description: Calcula el logaritmo natural.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Función D3DXQuaternionLn (D3DX10Math. h)
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
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678839"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="3d92a-103">Función D3DXQuaternionLn (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3d92a-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="3d92a-104">Calcula el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="3d92a-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d92a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d92a-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="3d92a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d92a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d92a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d92a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d92a-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d92a-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3d92a-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3d92a-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3d92a-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3d92a-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d92a-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d92a-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3d92a-112">Puntero a la estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="3d92a-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d92a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d92a-113">Return value</span></span>

<span data-ttu-id="3d92a-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d92a-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3d92a-115">Puntero a una estructura D3DXQUATERNION que es el logaritmo natural.</span><span class="sxs-lookup"><span data-stu-id="3d92a-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d92a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d92a-116">Remarks</span></span>

<span data-ttu-id="3d92a-117">La función D3DXQuaternionLn solo funciona para los cuaterniones de unidad.</span><span class="sxs-lookup"><span data-stu-id="3d92a-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="3d92a-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3d92a-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3d92a-119">De esta manera, la función D3DXQuaternionLn se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="3d92a-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3d92a-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="3d92a-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d92a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d92a-121">Requirements</span></span>



| <span data-ttu-id="3d92a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d92a-122">Requirement</span></span> | <span data-ttu-id="3d92a-123">Value</span><span class="sxs-lookup"><span data-stu-id="3d92a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d92a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d92a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3d92a-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d92a-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3d92a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d92a-126">Library</span></span><br/> | <dl> <span data-ttu-id="3d92a-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d92a-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d92a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d92a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d92a-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3d92a-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
