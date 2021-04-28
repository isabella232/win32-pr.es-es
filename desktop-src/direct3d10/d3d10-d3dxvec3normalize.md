---
description: 'Función D3DXVec3Normalize (D3DX10Math.h): devuelve la versión normalizada de un vector 3D.'
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Función D3DXVec3Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108183"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="37305-103">Función D3DXVec3Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="37305-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="37305-104">Devuelve la versión normalizada de un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="37305-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="37305-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37305-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="37305-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37305-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37305-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37305-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37305-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37305-109">Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="37305-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37305-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37305-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37305-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37305-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37305-112">Puntero a la estructura D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="37305-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37305-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37305-113">Return value</span></span>

<span data-ttu-id="37305-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37305-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37305-115">Puntero a una estructura D3DXVECTOR3 que es la versión normalizada del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="37305-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="37305-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37305-116">Remarks</span></span>

<span data-ttu-id="37305-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="37305-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="37305-118">De esta manera, la función D3DXVec3Normalize se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="37305-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37305-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37305-119">Requirements</span></span>



| <span data-ttu-id="37305-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37305-120">Requirement</span></span> | <span data-ttu-id="37305-121">Value</span><span class="sxs-lookup"><span data-stu-id="37305-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37305-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37305-122">Header</span></span><br/> | <dl> <span data-ttu-id="37305-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37305-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37305-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37305-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37305-125">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="37305-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
