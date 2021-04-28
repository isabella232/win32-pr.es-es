---
description: 'Función D3DXMatrixMultiplyTranspose (D3DX10Math.h): calcula el producto transpuesto de dos matrices.'
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Función D3DXMatrixMultiplyTranspose (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fcf3d5578aa6e2ad13bd3f91dfd2206d6eaf0b13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103423"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="1dea4-103">Función D3DXMatrixMultiplyTranspose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1dea4-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="1dea4-104">Calcula el producto transpuesto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="1dea4-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dea4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dea4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="1dea4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dea4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1dea4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dea4-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dea4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dea4-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1dea4-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1dea4-110">*pM1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1dea4-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dea4-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dea4-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dea4-112">Puntero a una estructura D3DXMATRIX de origen (lado izquierdo).</span><span class="sxs-lookup"><span data-stu-id="1dea4-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="1dea4-113">*pM2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1dea4-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dea4-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dea4-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dea4-115">Puntero a una estructura D3DXMATRIX de origen (lado derecho).</span><span class="sxs-lookup"><span data-stu-id="1dea4-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dea4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dea4-116">Return value</span></span>

<span data-ttu-id="1dea4-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dea4-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dea4-118">Puntero a una estructura D3DXMATRIX que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="1dea4-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dea4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1dea4-119">Remarks</span></span>

<span data-ttu-id="1dea4-120">El resultado es la transpuesta del producto de dos matrices de transformación, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="1dea4-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="1dea4-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1dea4-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1dea4-122">De esta manera, la función D3DXMatrixMultiplyTranspose se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="1dea4-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1dea4-123">Esta función es útil para establecer matrices como constantes para sombreadores de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="1dea4-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dea4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dea4-124">Requirements</span></span>



| <span data-ttu-id="1dea4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dea4-125">Requirement</span></span> | <span data-ttu-id="1dea4-126">Value</span><span class="sxs-lookup"><span data-stu-id="1dea4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dea4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dea4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1dea4-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1dea4-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1dea4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dea4-129">Library</span></span><br/> | <dl> <span data-ttu-id="1dea4-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dea4-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dea4-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1dea4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dea4-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1dea4-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
