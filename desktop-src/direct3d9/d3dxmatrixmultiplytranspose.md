---
description: Calcula el producto transpuesto de dos matrices.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Función D3DXMatrixMultiplyTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707736"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="eeea7-103">Función D3DXMatrixMultiplyTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eeea7-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="eeea7-104">Calcula el producto transpuesto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="eeea7-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeea7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeea7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="eeea7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeea7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eeea7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeea7-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eeea7-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eeea7-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eeea7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eeea7-110">*pM1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eeea7-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeea7-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="eeea7-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eeea7-112">Puntero a una estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="eeea7-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eeea7-113">*pM2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eeea7-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeea7-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="eeea7-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eeea7-115">Puntero a una estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="eeea7-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeea7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeea7-116">Return value</span></span>

<span data-ttu-id="eeea7-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eeea7-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eeea7-118">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="eeea7-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeea7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeea7-119">Remarks</span></span>

<span data-ttu-id="eeea7-120">El resultado es el transpuesto del producto de dos matrices de transformación, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="eeea7-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="eeea7-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="eeea7-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eeea7-122">De esta manera, la función **D3DXMatrixMultiplyTranspose** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="eeea7-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eeea7-123">Esta función resulta útil para establecer matrices como constantes para los sombreadores de píxeles y vértices.</span><span class="sxs-lookup"><span data-stu-id="eeea7-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeea7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeea7-124">Requirements</span></span>



| <span data-ttu-id="eeea7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeea7-125">Requirement</span></span> | <span data-ttu-id="eeea7-126">Value</span><span class="sxs-lookup"><span data-stu-id="eeea7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeea7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeea7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eeea7-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeea7-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eeea7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eeea7-129">Library</span></span><br/> | <dl> <span data-ttu-id="eeea7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeea7-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eeea7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeea7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeea7-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="eeea7-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eeea7-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="eeea7-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="eeea7-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="eeea7-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




