---
description: Calcula el inverso de una matriz.
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Función D3DXMatrixInverse (D3dx9math. h)
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
ms.openlocfilehash: eac1072c0174a03482e60167180f900588a13a72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717715"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="c88c3-103">Función D3DXMatrixInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c88c3-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="c88c3-104">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="c88c3-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c88c3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c88c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c88c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88c3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c88c3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c3-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88c3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c88c3-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c88c3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c88c3-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c88c3-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c3-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88c3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c88c3-112">Puntero a un valor FLOAT que contiene el determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c88c3-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="c88c3-113">Si el determinante no es necesario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="c88c3-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c88c3-114">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c88c3-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88c3-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c88c3-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c88c3-116">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c88c3-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88c3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c88c3-117">Return value</span></span>

<span data-ttu-id="c88c3-118">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88c3-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c88c3-119">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el inverso de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c88c3-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="c88c3-120">Si se produce un error en la inversion de matriz, se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="c88c3-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="c88c3-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="c88c3-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c88c3-122">De esta manera, la función **D3DXMatrixInverse** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c88c3-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88c3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88c3-123">Requirements</span></span>



| <span data-ttu-id="c88c3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88c3-124">Requirement</span></span> | <span data-ttu-id="c88c3-125">Value</span><span class="sxs-lookup"><span data-stu-id="c88c3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c88c3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c88c3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c88c3-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88c3-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c88c3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c88c3-128">Library</span></span><br/> | <dl> <span data-ttu-id="c88c3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c88c3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c88c3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c88c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88c3-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c88c3-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
