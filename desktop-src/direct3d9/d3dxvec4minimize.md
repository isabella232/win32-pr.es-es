---
description: Devuelve un vector 4D que se compone de los componentes más pequeños de dos vectores 4D.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: Función D3DXVec4Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707914"
---
# <a name="d3dxvec4minimize-function"></a><span data-ttu-id="2b35d-103">D3DXVec4Minimize función)</span><span class="sxs-lookup"><span data-stu-id="2b35d-103">D3DXVec4Minimize function</span></span>

<span data-ttu-id="2b35d-104">Devuelve un vector 4D que se compone de los componentes más pequeños de dos vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="2b35d-104">Returns a 4D vector that is made up of the smallest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b35d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b35d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2b35d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b35d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2b35d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35d-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b35d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2b35d-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2b35d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2b35d-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b35d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35d-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b35d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2b35d-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2b35d-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2b35d-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b35d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35d-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b35d-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2b35d-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2b35d-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b35d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b35d-116">Return value</span></span>

<span data-ttu-id="2b35d-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b35d-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2b35d-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que se compone de los componentes más pequeños de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="2b35d-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b35d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b35d-119">Remarks</span></span>

<span data-ttu-id="2b35d-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="2b35d-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2b35d-121">De esta manera, la función **D3DXVec4Minimize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="2b35d-121">In this way, the **D3DXVec4Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b35d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b35d-122">Requirements</span></span>



| <span data-ttu-id="2b35d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b35d-123">Requirement</span></span> | <span data-ttu-id="2b35d-124">Value</span><span class="sxs-lookup"><span data-stu-id="2b35d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b35d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b35d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2b35d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b35d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b35d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b35d-127">Library</span></span><br/> | <dl> <span data-ttu-id="2b35d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b35d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b35d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b35d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b35d-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2b35d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2b35d-131">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="2b35d-131">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
</dt> </dl>

 

 




