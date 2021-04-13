---
description: Escala un vector 2D.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: Función D3DXVec2Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362519"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="2cc08-103">D3DXVec2Scale función)</span><span class="sxs-lookup"><span data-stu-id="2cc08-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="2cc08-104">Escala un vector 2D.</span><span class="sxs-lookup"><span data-stu-id="2cc08-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc08-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cc08-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="2cc08-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cc08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc08-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2cc08-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc08-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cc08-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2cc08-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2cc08-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2cc08-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2cc08-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc08-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cc08-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2cc08-112">Puntero a la estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2cc08-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2cc08-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2cc08-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc08-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cc08-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cc08-115">Valor de escalado.</span><span class="sxs-lookup"><span data-stu-id="2cc08-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc08-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cc08-116">Return value</span></span>

<span data-ttu-id="2cc08-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cc08-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2cc08-118">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el vector escalado.</span><span class="sxs-lookup"><span data-stu-id="2cc08-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc08-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cc08-119">Remarks</span></span>

<span data-ttu-id="2cc08-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="2cc08-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2cc08-121">De esta manera, la función **D3DXVec2Scale** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="2cc08-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc08-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc08-122">Requirements</span></span>



| <span data-ttu-id="2cc08-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc08-123">Requirement</span></span> | <span data-ttu-id="2cc08-124">Value</span><span class="sxs-lookup"><span data-stu-id="2cc08-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc08-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cc08-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2cc08-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc08-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2cc08-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cc08-127">Library</span></span><br/> | <dl> <span data-ttu-id="2cc08-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cc08-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2cc08-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cc08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc08-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2cc08-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2cc08-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="2cc08-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="2cc08-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="2cc08-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
