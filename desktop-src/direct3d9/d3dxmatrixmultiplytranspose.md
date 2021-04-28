---
description: 'Función D3DXMatrixMultiplyTranspose (D3dx9math.h): calcula el producto transpuesto de dos matrices.'
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Función D3DXMatrixMultiplyTranspose (D3dx9math.h)
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
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107543"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="f3704-103">Función D3DXMatrixMultiplyTranspose (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f3704-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="f3704-104">Calcula el producto transpuesto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="f3704-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3704-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3704-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="f3704-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3704-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3704-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f3704-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3704-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3704-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3704-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f3704-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3704-110">*pM1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f3704-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3704-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3704-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3704-112">Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="f3704-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3704-113">*pM2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f3704-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3704-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3704-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3704-115">Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="f3704-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3704-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3704-116">Return value</span></span>

<span data-ttu-id="f3704-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3704-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3704-118">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="f3704-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3704-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3704-119">Remarks</span></span>

<span data-ttu-id="f3704-120">El resultado es la transpuesta del producto de dos matrices de transformación, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="f3704-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="f3704-121">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="f3704-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f3704-122">De esta manera, la **función D3DXMatrixMultiplyTranspose** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="f3704-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f3704-123">Esta función es útil para establecer matrices como constantes para sombreadores de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="f3704-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3704-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3704-124">Requirements</span></span>



| <span data-ttu-id="f3704-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3704-125">Requirement</span></span> | <span data-ttu-id="f3704-126">Value</span><span class="sxs-lookup"><span data-stu-id="f3704-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3704-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3704-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f3704-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f3704-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f3704-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3704-129">Library</span></span><br/> | <dl> <span data-ttu-id="f3704-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3704-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3704-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f3704-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3704-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f3704-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f3704-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="f3704-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="f3704-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="f3704-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




