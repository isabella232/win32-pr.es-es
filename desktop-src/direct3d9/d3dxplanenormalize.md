---
description: 'Función D3DXPlaneNormalize (D3dx9math.h): normaliza los coeficientes de plano para que el plano normal tenga longitud de unidad.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Función D3DXPlaneNormalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094153"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="7db33-103">Función D3DXPlaneNormalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="7db33-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="7db33-104">Normaliza los coeficientes del plano para que el plano normal tenga longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="7db33-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db33-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7db33-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="7db33-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7db33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db33-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7db33-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7db33-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7db33-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7db33-109">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7db33-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7db33-110">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7db33-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7db33-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="7db33-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7db33-112">Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) origen.</span><span class="sxs-lookup"><span data-stu-id="7db33-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db33-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7db33-113">Return value</span></span>

<span data-ttu-id="7db33-114">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7db33-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7db33-115">Puntero a una [**estructura D3DXPLANE**](d3dxplane.md) que representa la normalidad del plano.</span><span class="sxs-lookup"><span data-stu-id="7db33-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db33-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7db33-116">Remarks</span></span>

<span data-ttu-id="7db33-117">Esta función normaliza un plano para \| que a,b,c \| == 1.</span><span class="sxs-lookup"><span data-stu-id="7db33-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="7db33-118">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="7db33-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7db33-119">De esta manera, esta función se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="7db33-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db33-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7db33-120">Requirements</span></span>



| <span data-ttu-id="7db33-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7db33-121">Requirement</span></span> | <span data-ttu-id="7db33-122">Value</span><span class="sxs-lookup"><span data-stu-id="7db33-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7db33-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7db33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7db33-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7db33-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7db33-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7db33-125">Library</span></span><br/> | <dl> <span data-ttu-id="7db33-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7db33-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7db33-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7db33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db33-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7db33-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




