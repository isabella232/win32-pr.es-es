---
description: Calcula un cuaternión de longitud de unidad.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: Función D3DXQuaternionNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d052d4dfc88feb2a00237392071f63d724070b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547878"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="0dfd7-103">Función D3DXQuaternionNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0dfd7-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="0dfd7-104">Calcula un cuaternión de longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dfd7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dfd7-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="0dfd7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0dfd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dfd7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0dfd7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd7-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dfd7-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0dfd7-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0dfd7-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0dfd7-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd7-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0dfd7-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0dfd7-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dfd7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dfd7-113">Return value</span></span>

<span data-ttu-id="0dfd7-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dfd7-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0dfd7-115">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es la normal del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfd7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dfd7-116">Remarks</span></span>

<span data-ttu-id="0dfd7-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="0dfd7-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0dfd7-118">De esta manera, la función **D3DXQuaternionNormalize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dfd7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dfd7-119">Requirements</span></span>



| <span data-ttu-id="0dfd7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dfd7-120">Requirement</span></span> | <span data-ttu-id="0dfd7-121">Value</span><span class="sxs-lookup"><span data-stu-id="0dfd7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dfd7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dfd7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0dfd7-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd7-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0dfd7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0dfd7-124">Library</span></span><br/> | <dl> <span data-ttu-id="0dfd7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0dfd7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dfd7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dfd7-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0dfd7-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0dfd7-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="0dfd7-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




