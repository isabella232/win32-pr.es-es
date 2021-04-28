---
description: 'Función D3DXMatrixTranspose (D3DX10Math.h): devuelve la transpuesta de matriz de una matriz.'
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: Función D3DXMatrixTranspose (D3DX10Math.h)
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
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108863"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="16941-103">Función D3DXMatrixTranspose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="16941-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="16941-104">Devuelve la transpuesta de matriz de una matriz.</span><span class="sxs-lookup"><span data-stu-id="16941-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="16941-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16941-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="16941-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16941-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16941-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16941-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16941-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16941-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="16941-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16941-110">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="16941-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16941-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="16941-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16941-112">Puntero a la estructura D3DXMATRIX de origen.</span><span class="sxs-lookup"><span data-stu-id="16941-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16941-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16941-113">Return value</span></span>

<span data-ttu-id="16941-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16941-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16941-115">Puntero a la estructura D3DXMATRIX que es la transpuesta de matriz de la matriz.</span><span class="sxs-lookup"><span data-stu-id="16941-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="16941-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16941-116">Remarks</span></span>

<span data-ttu-id="16941-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="16941-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="16941-118">De este modo, la función D3DXMatrixTranspose se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="16941-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16941-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16941-119">Requirements</span></span>



| <span data-ttu-id="16941-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16941-120">Requirement</span></span> | <span data-ttu-id="16941-121">Value</span><span class="sxs-lookup"><span data-stu-id="16941-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16941-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16941-122">Header</span></span><br/>  | <dl> <span data-ttu-id="16941-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="16941-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="16941-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16941-124">Library</span></span><br/> | <dl> <span data-ttu-id="16941-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="16941-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16941-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16941-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16941-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="16941-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
