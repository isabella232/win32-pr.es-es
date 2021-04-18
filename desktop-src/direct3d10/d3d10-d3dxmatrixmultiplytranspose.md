---
description: Calcula el producto transpuesto de dos matrices.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Función D3DXMatrixMultiplyTranspose (D3DX10Math. h)
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
ms.openlocfilehash: 187912a4117ab502ea7b0b1b3fc1ea105ecbc3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721535"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="afed6-103">Función D3DXMatrixMultiplyTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="afed6-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="afed6-104">Calcula el producto transpuesto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="afed6-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="afed6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afed6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="afed6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afed6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afed6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="afed6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="afed6-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="afed6-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afed6-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="afed6-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="afed6-110">*pM1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afed6-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afed6-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="afed6-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afed6-112">Puntero a una estructura D3DXMATRIX de origen (lado izquierdo).</span><span class="sxs-lookup"><span data-stu-id="afed6-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="afed6-113">*pM2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afed6-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afed6-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="afed6-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afed6-115">Puntero a una estructura de D3DXMATRIX de origen (lado derecho).</span><span class="sxs-lookup"><span data-stu-id="afed6-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afed6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afed6-116">Return value</span></span>

<span data-ttu-id="afed6-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="afed6-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afed6-118">Puntero a una estructura D3DXMATRIX que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="afed6-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="afed6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afed6-119">Remarks</span></span>

<span data-ttu-id="afed6-120">El resultado es el transpuesto del producto de dos matrices de transformación, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="afed6-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="afed6-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="afed6-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="afed6-122">De esta manera, la función D3DXMatrixMultiplyTranspose se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="afed6-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="afed6-123">Esta función resulta útil para establecer matrices como constantes para los sombreadores de píxeles y vértices.</span><span class="sxs-lookup"><span data-stu-id="afed6-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="afed6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afed6-124">Requirements</span></span>



| <span data-ttu-id="afed6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="afed6-125">Requirement</span></span> | <span data-ttu-id="afed6-126">Value</span><span class="sxs-lookup"><span data-stu-id="afed6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afed6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afed6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="afed6-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="afed6-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="afed6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afed6-129">Library</span></span><br/> | <dl> <span data-ttu-id="afed6-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afed6-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afed6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="afed6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afed6-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="afed6-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
