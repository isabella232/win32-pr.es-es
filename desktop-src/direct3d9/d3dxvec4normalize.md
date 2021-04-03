---
description: Devuelve la versión normalizada de un vector 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Función D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083819"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="cf683-103">Función D3DXVec4Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cf683-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="cf683-104">Devuelve la versión normalizada de un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="cf683-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf683-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf683-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="cf683-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf683-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf683-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf683-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf683-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="cf683-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cf683-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cf683-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf683-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf683-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cf683-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="cf683-112">Puntero a la estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="cf683-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf683-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf683-113">Return value</span></span>

<span data-ttu-id="cf683-114">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf683-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="cf683-115">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="cf683-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf683-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf683-116">Remarks</span></span>

<span data-ttu-id="cf683-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="cf683-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cf683-118">De esta manera, la función **D3DXVec4Normalize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="cf683-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf683-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf683-119">Requirements</span></span>



| <span data-ttu-id="cf683-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf683-120">Requirement</span></span> | <span data-ttu-id="cf683-121">Value</span><span class="sxs-lookup"><span data-stu-id="cf683-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf683-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf683-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cf683-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf683-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cf683-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf683-124">Library</span></span><br/> | <dl> <span data-ttu-id="cf683-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf683-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf683-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf683-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf683-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="cf683-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




