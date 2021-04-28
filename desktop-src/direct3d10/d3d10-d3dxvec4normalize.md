---
description: 'Función D3DXVec4Normalize (D3DX10Math.h): devuelve la versión normalizada de un vector 4D.'
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Función D3DXVec4Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102913"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="a9c23-103">Función D3DXVec4Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="a9c23-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="a9c23-104">Devuelve la versión normalizada de un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="a9c23-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9c23-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="a9c23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9c23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c23-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a9c23-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c23-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9c23-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a9c23-109">Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a9c23-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9c23-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a9c23-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c23-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9c23-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a9c23-112">Puntero a la estructura D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="a9c23-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c23-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9c23-113">Return value</span></span>

<span data-ttu-id="a9c23-114">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9c23-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a9c23-115">Puntero a una estructura D3DXVECTOR4 que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="a9c23-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c23-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9c23-116">Remarks</span></span>

<span data-ttu-id="a9c23-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="a9c23-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a9c23-118">De esta manera, la función D3DXVec4Normalize se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="a9c23-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c23-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c23-119">Requirements</span></span>



| <span data-ttu-id="a9c23-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c23-120">Requirement</span></span> | <span data-ttu-id="a9c23-121">Value</span><span class="sxs-lookup"><span data-stu-id="a9c23-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c23-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9c23-122">Header</span></span><br/> | <dl> <span data-ttu-id="a9c23-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c23-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c23-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9c23-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c23-125">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a9c23-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
