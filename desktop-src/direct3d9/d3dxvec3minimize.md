---
description: Devuelve un vector 3D que se compone de los componentes más pequeños de dos vectores 3D.
ms.assetid: f38164a5-d016-4a8a-a7fe-d7eb0a681107
title: Función D3DXVec3Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 532c3cfaddc63b0f358fa3ce88afeccc2f12e289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083810"
---
# <a name="d3dxvec3minimize-function"></a><span data-ttu-id="7250a-103">D3DXVec3Minimize función)</span><span class="sxs-lookup"><span data-stu-id="7250a-103">D3DXVec3Minimize function</span></span>

<span data-ttu-id="7250a-104">Devuelve un vector 3D que se compone de los componentes más pequeños de dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="7250a-104">Returns a 3D vector that is made up of the smallest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7250a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7250a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Minimize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="7250a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7250a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7250a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7250a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7250a-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7250a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7250a-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7250a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7250a-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7250a-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7250a-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7250a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7250a-112">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="7250a-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7250a-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7250a-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7250a-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7250a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7250a-115">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="7250a-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7250a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7250a-116">Return value</span></span>

<span data-ttu-id="7250a-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7250a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7250a-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que se compone de los componentes más pequeños de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="7250a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7250a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7250a-119">Remarks</span></span>

<span data-ttu-id="7250a-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="7250a-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7250a-121">De esta manera, la función **D3DXVec3Minimize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="7250a-121">In this way, the **D3DXVec3Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7250a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7250a-122">Requirements</span></span>



| <span data-ttu-id="7250a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7250a-123">Requirement</span></span> | <span data-ttu-id="7250a-124">Value</span><span class="sxs-lookup"><span data-stu-id="7250a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7250a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7250a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7250a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7250a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7250a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7250a-127">Library</span></span><br/> | <dl> <span data-ttu-id="7250a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7250a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7250a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7250a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7250a-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7250a-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7250a-131">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="7250a-131">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
</dt> </dl>

 

 




