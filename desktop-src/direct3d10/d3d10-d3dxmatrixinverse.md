---
description: 'Función D3DXMatrixInverse (D3DX10Math.h): calcula el inverso de una matriz.'
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: Función D3DXMatrixInverse (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6b42cf0ae3f9ee1154d385600b00a2dcb10c4fd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113203"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="5eacf-103">Función D3DXMatrixInverse (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="5eacf-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="5eacf-104">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="5eacf-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eacf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5eacf-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5eacf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5eacf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eacf-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5eacf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eacf-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5eacf-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5eacf-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5eacf-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5eacf-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5eacf-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eacf-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5eacf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5eacf-112">Puntero a un valor FLOAT que contiene el determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5eacf-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="5eacf-113">Si el determinante no es necesario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="5eacf-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5eacf-114">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5eacf-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eacf-115">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5eacf-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5eacf-116">Puntero a la estructura D3DXMATRIX de origen.</span><span class="sxs-lookup"><span data-stu-id="5eacf-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eacf-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5eacf-117">Return value</span></span>

<span data-ttu-id="5eacf-118">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5eacf-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5eacf-119">Puntero a una estructura D3DXMATRIX que es el inverso de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5eacf-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="5eacf-120">Si se produce un error en la inversión de matriz, **se devuelve NULL.**</span><span class="sxs-lookup"><span data-stu-id="5eacf-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="5eacf-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="5eacf-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5eacf-122">De este modo, la función D3DXMatrixInverse se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="5eacf-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eacf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eacf-123">Requirements</span></span>



| <span data-ttu-id="5eacf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eacf-124">Requirement</span></span> | <span data-ttu-id="5eacf-125">Value</span><span class="sxs-lookup"><span data-stu-id="5eacf-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eacf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5eacf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5eacf-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5eacf-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5eacf-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5eacf-128">Library</span></span><br/> | <dl> <span data-ttu-id="5eacf-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eacf-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5eacf-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5eacf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eacf-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="5eacf-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
