---
description: Devuelve un vector 2D formado por los componentes más pequeños de dos vectores 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: Función D3DXVec2Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707815"
---
# <a name="d3dxvec2minimize-function"></a><span data-ttu-id="091d1-103">D3DXVec2Minimize función)</span><span class="sxs-lookup"><span data-stu-id="091d1-103">D3DXVec2Minimize function</span></span>

<span data-ttu-id="091d1-104">Devuelve un vector 2D formado por los componentes más pequeños de dos vectores 2D.</span><span class="sxs-lookup"><span data-stu-id="091d1-104">Returns a 2D vector that is made up of the smallest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="091d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="091d1-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="091d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="091d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="091d1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="091d1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="091d1-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="091d1-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="091d1-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="091d1-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="091d1-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="091d1-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091d1-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="091d1-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="091d1-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="091d1-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="091d1-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="091d1-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091d1-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="091d1-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="091d1-115">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="091d1-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="091d1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="091d1-116">Return value</span></span>

<span data-ttu-id="091d1-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="091d1-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="091d1-118">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que se compone de los componentes más pequeños de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="091d1-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="091d1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="091d1-119">Remarks</span></span>

<span data-ttu-id="091d1-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="091d1-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="091d1-121">De esta manera, la función **D3DXVec2Minimize** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="091d1-121">In this way, the **D3DXVec2Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="091d1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091d1-122">Requirements</span></span>



| <span data-ttu-id="091d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="091d1-123">Requirement</span></span> | <span data-ttu-id="091d1-124">Value</span><span class="sxs-lookup"><span data-stu-id="091d1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="091d1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="091d1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="091d1-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="091d1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="091d1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="091d1-127">Library</span></span><br/> | <dl> <span data-ttu-id="091d1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="091d1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="091d1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="091d1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="091d1-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="091d1-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="091d1-131">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="091d1-131">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
</dt> </dl>

 

 




