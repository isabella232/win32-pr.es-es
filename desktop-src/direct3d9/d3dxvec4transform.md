---
description: 'Función D3DXVec4Transform (D3dx9math.h): transforma un vector 4D mediante una matriz determinada.'
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Función D3DXVec4Transform (D3dx9math.h)
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
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115513"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="1dd46-103">Función D3DXVec4Transform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1dd46-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="1dd46-104">Transforma un vector 4D mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="1dd46-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd46-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dd46-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1dd46-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dd46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd46-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1dd46-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd46-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dd46-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dd46-109">Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1dd46-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1dd46-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1dd46-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd46-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dd46-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dd46-112">Puntero a la estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen.</span><span class="sxs-lookup"><span data-stu-id="1dd46-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1dd46-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1dd46-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd46-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dd46-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dd46-115">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="1dd46-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd46-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dd46-116">Return value</span></span>

<span data-ttu-id="1dd46-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dd46-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dd46-118">Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el vector 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="1dd46-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd46-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1dd46-119">Remarks</span></span>

<span data-ttu-id="1dd46-120">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1dd46-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1dd46-121">De esta manera, la **función D3DXVec4Transform** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="1dd46-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd46-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dd46-122">Requirements</span></span>



| <span data-ttu-id="1dd46-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd46-123">Requirement</span></span> | <span data-ttu-id="1dd46-124">Value</span><span class="sxs-lookup"><span data-stu-id="1dd46-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd46-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dd46-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1dd46-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd46-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1dd46-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dd46-127">Library</span></span><br/> | <dl> <span data-ttu-id="1dd46-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dd46-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dd46-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1dd46-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd46-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1dd46-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




