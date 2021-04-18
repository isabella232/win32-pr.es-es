---
description: Devuelve la transposición de la matriz de una matriz.
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: Función D3DXMatrixTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0ecc93a560e15b8f0abe4337b866efc292c9355e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721522"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="68c4b-103">Función D3DXMatrixTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="68c4b-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="68c4b-104">Devuelve la transposición de la matriz de una matriz.</span><span class="sxs-lookup"><span data-stu-id="68c4b-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68c4b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="68c4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c4b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="68c4b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68c4b-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="68c4b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68c4b-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="68c4b-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="68c4b-110">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68c4b-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68c4b-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="68c4b-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68c4b-112">Puntero a la estructura de D3DXMATRIX de origen.</span><span class="sxs-lookup"><span data-stu-id="68c4b-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c4b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68c4b-113">Return value</span></span>

<span data-ttu-id="68c4b-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="68c4b-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68c4b-115">Puntero a la estructura D3DXMATRIX que es la transposición de la matriz.</span><span class="sxs-lookup"><span data-stu-id="68c4b-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c4b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68c4b-116">Remarks</span></span>

<span data-ttu-id="68c4b-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="68c4b-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="68c4b-118">De esta manera, la función D3DXMatrixTranspose se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="68c4b-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c4b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c4b-119">Requirements</span></span>



| <span data-ttu-id="68c4b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c4b-120">Requirement</span></span> | <span data-ttu-id="68c4b-121">Value</span><span class="sxs-lookup"><span data-stu-id="68c4b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68c4b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68c4b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="68c4b-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68c4b-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="68c4b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68c4b-124">Library</span></span><br/> | <dl> <span data-ttu-id="68c4b-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68c4b-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68c4b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="68c4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c4b-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="68c4b-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
