---
description: 'Función D3DXQuaternionNormalize (D3DX10Math.h): calcula un cuaternión de longitud de unidad.'
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Función D3DXQuaternionNormalize (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103143"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="de723-103">Función D3DXQuaternionNormalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="de723-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="de723-104">Calcula un cuaternión de longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="de723-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="de723-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de723-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="de723-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de723-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de723-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de723-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de723-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="de723-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="de723-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="de723-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="de723-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="de723-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de723-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="de723-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="de723-112">Puntero a la estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="de723-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de723-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de723-113">Return value</span></span>

<span data-ttu-id="de723-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="de723-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="de723-115">Puntero a una estructura D3DXQUATERNION que es la normal del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="de723-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="de723-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de723-116">Remarks</span></span>

<span data-ttu-id="de723-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="de723-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="de723-118">De este modo, la función D3DXQuaternionNormalize se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="de723-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de723-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de723-119">Requirements</span></span>



| <span data-ttu-id="de723-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="de723-120">Requirement</span></span> | <span data-ttu-id="de723-121">Value</span><span class="sxs-lookup"><span data-stu-id="de723-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de723-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de723-122">Header</span></span><br/>  | <dl> <span data-ttu-id="de723-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="de723-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="de723-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de723-124">Library</span></span><br/> | <dl> <span data-ttu-id="de723-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="de723-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de723-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de723-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de723-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="de723-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
