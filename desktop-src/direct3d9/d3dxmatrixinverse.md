---
description: 'Función D3DXMatrixInverse (D3dx9math.h): calcula el inverso de una matriz.'
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Función D3DXMatrixInverse (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098153"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="c249c-103">Función D3DXMatrixInverse (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c249c-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="c249c-104">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="c249c-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c249c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c249c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c249c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c249c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c249c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c249c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c249c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c249c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c249c-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c249c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c249c-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c249c-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c249c-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c249c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c249c-112">Puntero a un valor FLOAT que contiene el determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c249c-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="c249c-113">Si el determinante no es necesario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c249c-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c249c-114">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c249c-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c249c-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c249c-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c249c-116">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="c249c-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c249c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c249c-117">Return value</span></span>

<span data-ttu-id="c249c-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c249c-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c249c-119">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es la inversa de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c249c-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="c249c-120">Si se produce un error en la inversión de matriz, se devuelve **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c249c-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="c249c-121">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="c249c-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c249c-122">De este modo, la **función D3DXMatrixInverse** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c249c-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c249c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c249c-123">Requirements</span></span>



| <span data-ttu-id="c249c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c249c-124">Requirement</span></span> | <span data-ttu-id="c249c-125">Value</span><span class="sxs-lookup"><span data-stu-id="c249c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c249c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c249c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c249c-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c249c-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c249c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c249c-128">Library</span></span><br/> | <dl> <span data-ttu-id="c249c-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c249c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c249c-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c249c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c249c-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c249c-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
