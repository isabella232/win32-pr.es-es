---
description: Calcula el inverso de una matriz.
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: Función D3DXMatrixInverse (D3DX10Math. h)
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
ms.openlocfilehash: cc075609ea118e12b46846f649d689f6fbc2caf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548083"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="eefe0-103">Función D3DXMatrixInverse (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="eefe0-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="eefe0-104">Calcula el inverso de una matriz.</span><span class="sxs-lookup"><span data-stu-id="eefe0-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefe0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eefe0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="eefe0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eefe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefe0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eefe0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eefe0-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eefe0-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eefe0-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eefe0-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eefe0-110">*pDeterminant* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eefe0-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eefe0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eefe0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eefe0-112">Puntero a un valor FLOAT que contiene el determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="eefe0-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="eefe0-113">Si el determinante no es necesario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="eefe0-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eefe0-114">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eefe0-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eefe0-115">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="eefe0-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eefe0-116">Puntero a la estructura de D3DXMATRIX de origen.</span><span class="sxs-lookup"><span data-stu-id="eefe0-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefe0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eefe0-117">Return value</span></span>

<span data-ttu-id="eefe0-118">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eefe0-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eefe0-119">Puntero a una estructura D3DXMATRIX que es el inverso de la matriz.</span><span class="sxs-lookup"><span data-stu-id="eefe0-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="eefe0-120">Si se produce un error en la inversion de matriz, se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="eefe0-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="eefe0-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="eefe0-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eefe0-122">De esta manera, la función D3DXMatrixInverse se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="eefe0-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eefe0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eefe0-123">Requirements</span></span>



| <span data-ttu-id="eefe0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eefe0-124">Requirement</span></span> | <span data-ttu-id="eefe0-125">Value</span><span class="sxs-lookup"><span data-stu-id="eefe0-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eefe0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eefe0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eefe0-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eefe0-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="eefe0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eefe0-128">Library</span></span><br/> | <dl> <span data-ttu-id="eefe0-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eefe0-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eefe0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="eefe0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefe0-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="eefe0-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
