---
description: Calcula un cuaternión de longitud de unidad.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Función D3DXQuaternionNormalize (D3DX10Math. h)
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
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280430"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="735e9-103">Función D3DXQuaternionNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="735e9-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="735e9-104">Calcula un cuaternión de longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="735e9-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="735e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="735e9-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="735e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="735e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="735e9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="735e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="735e9-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="735e9-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="735e9-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="735e9-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="735e9-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="735e9-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="735e9-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="735e9-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="735e9-112">Puntero a la estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="735e9-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="735e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="735e9-113">Return value</span></span>

<span data-ttu-id="735e9-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="735e9-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="735e9-115">Puntero a una estructura D3DXQUATERNION que es la normal del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="735e9-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="735e9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="735e9-116">Remarks</span></span>

<span data-ttu-id="735e9-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="735e9-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="735e9-118">De esta manera, la función D3DXQuaternionNormalize se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="735e9-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="735e9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="735e9-119">Requirements</span></span>



| <span data-ttu-id="735e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="735e9-120">Requirement</span></span> | <span data-ttu-id="735e9-121">Value</span><span class="sxs-lookup"><span data-stu-id="735e9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="735e9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="735e9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="735e9-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="735e9-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="735e9-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="735e9-124">Library</span></span><br/> | <dl> <span data-ttu-id="735e9-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="735e9-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="735e9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="735e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735e9-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="735e9-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
