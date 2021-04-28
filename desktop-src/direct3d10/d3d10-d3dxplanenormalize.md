---
description: 'Función D3DXPlaneNormalize (D3DX10Math.h): normaliza los coeficientes de plano para que el plano normal tenga longitud de unidad.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Función D3DXPlaneNormalize (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8b3499297a008b0d8f5dc705080bbd1d5bbe3af4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103313"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="586db-103">Función D3DXPlaneNormalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="586db-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="586db-104">Normaliza los coeficientes del plano para que el plano normal tenga longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="586db-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="586db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="586db-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="586db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="586db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586db-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="586db-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="586db-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="586db-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="586db-109">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="586db-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="586db-110">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="586db-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="586db-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="586db-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="586db-112">Puntero a la estructura D3DXPLANE de origen.</span><span class="sxs-lookup"><span data-stu-id="586db-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586db-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="586db-113">Return value</span></span>

<span data-ttu-id="586db-114">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="586db-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="586db-115">Puntero a una estructura D3DXPLANE que representa la normalidad del plano.</span><span class="sxs-lookup"><span data-stu-id="586db-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="586db-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="586db-116">Remarks</span></span>

<span data-ttu-id="586db-117">Esta función normaliza un plano para que \| a,b,c \| == 1.</span><span class="sxs-lookup"><span data-stu-id="586db-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="586db-118">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="586db-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="586db-119">De esta manera, esta función se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="586db-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="586db-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="586db-120">Requirements</span></span>



| <span data-ttu-id="586db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="586db-121">Requirement</span></span> | <span data-ttu-id="586db-122">Value</span><span class="sxs-lookup"><span data-stu-id="586db-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="586db-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="586db-123">Header</span></span><br/>  | <dl> <span data-ttu-id="586db-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="586db-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="586db-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="586db-125">Library</span></span><br/> | <dl> <span data-ttu-id="586db-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="586db-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="586db-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="586db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586db-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="586db-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
