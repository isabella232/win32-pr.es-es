---
description: Determina el producto de dos matrices.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Función D3DXMatrixMultiply (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707737"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="4e814-103">Función D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4e814-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="4e814-104">Determina el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="4e814-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e814-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e814-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="4e814-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e814-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e814-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e814-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e814-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e814-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e814-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4e814-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4e814-110">*pM1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e814-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e814-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e814-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e814-112">Puntero a una estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="4e814-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e814-113">*pM2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e814-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e814-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e814-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e814-115">Puntero a una estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="4e814-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e814-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e814-116">Return value</span></span>

<span data-ttu-id="4e814-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e814-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e814-118">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="4e814-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e814-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e814-119">Remarks</span></span>

<span data-ttu-id="4e814-120">El resultado representa la transformación M1 seguida de la transformación m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="4e814-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="4e814-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="4e814-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4e814-122">De esta manera, la función **D3DXMatrixMultiply** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="4e814-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e814-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e814-123">Requirements</span></span>



| <span data-ttu-id="4e814-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e814-124">Requirement</span></span> | <span data-ttu-id="4e814-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e814-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e814-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e814-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4e814-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e814-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4e814-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e814-128">Library</span></span><br/> | <dl> <span data-ttu-id="4e814-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e814-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e814-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e814-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e814-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4e814-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4e814-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="4e814-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




