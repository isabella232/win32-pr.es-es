---
description: Devuelve un vector 4D que se compone de los componentes más grandes de dos vectores 4D.
ms.assetid: a08ceba0-938c-42af-8f32-b1fd8c12d926
title: Función D3DXVec4Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c145094deec5bdfdca123e6e494b18bbee01ce5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280529"
---
# <a name="d3dxvec4maximize-function"></a><span data-ttu-id="e2304-103">D3DXVec4Maximize función)</span><span class="sxs-lookup"><span data-stu-id="e2304-103">D3DXVec4Maximize function</span></span>

<span data-ttu-id="e2304-104">Devuelve un vector 4D que se compone de los componentes más grandes de dos vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="e2304-104">Returns a 4D vector that is made up of the largest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2304-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2304-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Maximize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e2304-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2304-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2304-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2304-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2304-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e2304-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e2304-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2304-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2304-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2304-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2304-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e2304-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e2304-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2304-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2304-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2304-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2304-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e2304-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e2304-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2304-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2304-116">Return value</span></span>

<span data-ttu-id="e2304-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2304-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e2304-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que se compone de los componentes más grandes de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="e2304-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2304-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2304-119">Remarks</span></span>

<span data-ttu-id="e2304-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="e2304-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e2304-121">De esta manera, la función **D3DXVec4Maximize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e2304-121">In this way, the **D3DXVec4Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2304-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2304-122">Requirements</span></span>



| <span data-ttu-id="e2304-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2304-123">Requirement</span></span> | <span data-ttu-id="e2304-124">Value</span><span class="sxs-lookup"><span data-stu-id="e2304-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2304-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2304-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e2304-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2304-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e2304-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2304-127">Library</span></span><br/> | <dl> <span data-ttu-id="e2304-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2304-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2304-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2304-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2304-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e2304-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e2304-131">**D3DXVec4Minimize**</span><span class="sxs-lookup"><span data-stu-id="e2304-131">**D3DXVec4Minimize**</span></span>](d3dxvec4minimize.md)
</dt> </dl>

 

 




