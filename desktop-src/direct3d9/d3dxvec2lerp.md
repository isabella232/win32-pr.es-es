---
description: Realiza una interpolación lineal entre dos vectores 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Función D3DXVec2Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707816"
---
# <a name="d3dxvec2lerp-function"></a><span data-ttu-id="f2442-103">D3DXVec2Lerp función)</span><span class="sxs-lookup"><span data-stu-id="f2442-103">D3DXVec2Lerp function</span></span>

<span data-ttu-id="f2442-104">Realiza una interpolación lineal entre dos vectores 2D.</span><span class="sxs-lookup"><span data-stu-id="f2442-104">Performs a linear interpolation between two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2442-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2442-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="f2442-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2442-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f2442-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2442-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2442-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2442-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2442-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f2442-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2442-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2442-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2442-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2442-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="f2442-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2442-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2442-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2442-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2442-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2442-115">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="f2442-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2442-116">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f2442-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2442-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2442-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2442-118">Parámetro que se interpola linealmente entre los vectores.</span><span class="sxs-lookup"><span data-stu-id="f2442-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2442-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2442-119">Return value</span></span>

<span data-ttu-id="f2442-120">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2442-120">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2442-121">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="f2442-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2442-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2442-122">Remarks</span></span>

<span data-ttu-id="f2442-123">Esta función realiza la interpolación lineal basada en la siguiente fórmula: v1 + s (V2-V1).</span><span class="sxs-lookup"><span data-stu-id="f2442-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="f2442-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="f2442-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f2442-125">De esta manera, la función **D3DXVec2Lerp** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f2442-125">In this way, the **D3DXVec2Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2442-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2442-126">Requirements</span></span>



| <span data-ttu-id="f2442-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2442-127">Requirement</span></span> | <span data-ttu-id="f2442-128">Value</span><span class="sxs-lookup"><span data-stu-id="f2442-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2442-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2442-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f2442-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2442-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2442-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2442-131">Library</span></span><br/> | <dl> <span data-ttu-id="f2442-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2442-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2442-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2442-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2442-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f2442-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
