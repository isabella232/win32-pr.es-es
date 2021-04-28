---
description: 'Función D3DXMatrixTranspose (D3dx9math.h): devuelve la transpuesta de matriz de una matriz.'
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: Función D3DXMatrixTranspose (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098113"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="a8144-103">Función D3DXMatrixTranspose (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a8144-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="a8144-104">Devuelve la transpuesta de matriz de una matriz.</span><span class="sxs-lookup"><span data-stu-id="a8144-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8144-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8144-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a8144-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8144-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8144-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a8144-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8144-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8144-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8144-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a8144-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a8144-110">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8144-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8144-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8144-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8144-112">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="a8144-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8144-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8144-113">Return value</span></span>

<span data-ttu-id="a8144-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8144-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8144-115">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es la transpuesta de matriz de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a8144-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8144-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8144-116">Remarks</span></span>

<span data-ttu-id="a8144-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="a8144-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a8144-118">De esta manera, la **función D3DXMatrixTranspose** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="a8144-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8144-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8144-119">Requirements</span></span>



| <span data-ttu-id="a8144-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8144-120">Requirement</span></span> | <span data-ttu-id="a8144-121">Value</span><span class="sxs-lookup"><span data-stu-id="a8144-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8144-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8144-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a8144-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a8144-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8144-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8144-124">Library</span></span><br/> | <dl> <span data-ttu-id="a8144-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8144-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8144-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8144-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8144-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a8144-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




