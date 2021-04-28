---
description: 'Función D3DXVec4Normalize (D3dx9math.h): devuelve la versión normalizada de un vector 4D.'
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Función D3DXVec4Normalize (D3dx9math.h)
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
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097663"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="5d47f-103">Función D3DXVec4Normalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5d47f-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="5d47f-104">Devuelve la versión normalizada de un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="5d47f-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d47f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d47f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="5d47f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d47f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d47f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5d47f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47f-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d47f-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5d47f-109">Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5d47f-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5d47f-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5d47f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47f-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d47f-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5d47f-112">Puntero a la estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen.</span><span class="sxs-lookup"><span data-stu-id="5d47f-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d47f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d47f-113">Return value</span></span>

<span data-ttu-id="5d47f-114">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d47f-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5d47f-115">Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="5d47f-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d47f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d47f-116">Remarks</span></span>

<span data-ttu-id="5d47f-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="5d47f-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5d47f-118">De esta manera, la **función D3DXVec4Normalize** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="5d47f-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d47f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d47f-119">Requirements</span></span>



| <span data-ttu-id="5d47f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d47f-120">Requirement</span></span> | <span data-ttu-id="5d47f-121">Value</span><span class="sxs-lookup"><span data-stu-id="5d47f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d47f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d47f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5d47f-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5d47f-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5d47f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d47f-124">Library</span></span><br/> | <dl> <span data-ttu-id="5d47f-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d47f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d47f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5d47f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d47f-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="5d47f-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




