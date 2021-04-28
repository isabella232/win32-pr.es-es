---
description: 'Función D3DXQuaternionNormalize (D3dx9math.h): calcula un cuaternión de longitud de unidad.'
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: Función D3DXQuaternionNormalize (D3dx9math.h)
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
ms.openlocfilehash: a5d4a7938b96d3d8693fd2091fcbd4f664f465c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094043"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="37ee3-103">Función D3DXQuaternionNormalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="37ee3-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="37ee3-104">Calcula un cuaternión de longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="37ee3-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ee3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37ee3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="37ee3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37ee3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ee3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37ee3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ee3-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="37ee3-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="37ee3-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="37ee3-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37ee3-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37ee3-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ee3-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="37ee3-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="37ee3-112">Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="37ee3-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ee3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37ee3-113">Return value</span></span>

<span data-ttu-id="37ee3-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="37ee3-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="37ee3-115">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es la normal del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="37ee3-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ee3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37ee3-116">Remarks</span></span>

<span data-ttu-id="37ee3-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="37ee3-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="37ee3-118">De este modo, la **función D3DXQuaternionNormalize** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="37ee3-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ee3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ee3-119">Requirements</span></span>



| <span data-ttu-id="37ee3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ee3-120">Requirement</span></span> | <span data-ttu-id="37ee3-121">Value</span><span class="sxs-lookup"><span data-stu-id="37ee3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ee3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37ee3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="37ee3-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37ee3-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="37ee3-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37ee3-124">Library</span></span><br/> | <dl> <span data-ttu-id="37ee3-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="37ee3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37ee3-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37ee3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ee3-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="37ee3-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="37ee3-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="37ee3-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




