---
description: Transforma un vector 4D por una matriz determinada.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Función D3DXVec4Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20192cf51a6096bbbce1f009d91d96551aec12d8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707997"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="c55ce-103">Función D3DXVec4Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c55ce-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="c55ce-104">Transforma un vector 4D por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="c55ce-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c55ce-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c55ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c55ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55ce-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c55ce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c55ce-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c55ce-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c55ce-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c55ce-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c55ce-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c55ce-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55ce-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c55ce-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c55ce-112">Puntero a la estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c55ce-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c55ce-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c55ce-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55ce-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c55ce-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c55ce-115">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c55ce-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55ce-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c55ce-116">Return value</span></span>

<span data-ttu-id="c55ce-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c55ce-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c55ce-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el vector 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="c55ce-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55ce-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c55ce-119">Remarks</span></span>

<span data-ttu-id="c55ce-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="c55ce-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c55ce-121">De esta manera, la función **D3DXVec4Transform** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c55ce-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55ce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c55ce-122">Requirements</span></span>



| <span data-ttu-id="c55ce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55ce-123">Requirement</span></span> | <span data-ttu-id="c55ce-124">Value</span><span class="sxs-lookup"><span data-stu-id="c55ce-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55ce-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c55ce-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c55ce-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c55ce-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c55ce-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c55ce-127">Library</span></span><br/> | <dl> <span data-ttu-id="c55ce-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c55ce-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c55ce-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c55ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55ce-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c55ce-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




