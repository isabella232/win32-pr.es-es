---
description: Normaliza los coeficientes del plano para que el plano normal tenga una longitud de unidad.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Función D3DXPlaneNormalize (D3DX10Math. h)
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
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721517"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="9920f-103">Función D3DXPlaneNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9920f-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="9920f-104">Normaliza los coeficientes del plano para que el plano normal tenga una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="9920f-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="9920f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9920f-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="9920f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9920f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9920f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9920f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9920f-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="9920f-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="9920f-109">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="9920f-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9920f-110">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9920f-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9920f-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="9920f-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="9920f-112">Puntero a la estructura de D3DXPLANE de origen.</span><span class="sxs-lookup"><span data-stu-id="9920f-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9920f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9920f-113">Return value</span></span>

<span data-ttu-id="9920f-114">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="9920f-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="9920f-115">Puntero a una estructura D3DXPLANE que representa el normal del plano.</span><span class="sxs-lookup"><span data-stu-id="9920f-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="9920f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9920f-116">Remarks</span></span>

<span data-ttu-id="9920f-117">Esta función normaliza un plano para que \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="9920f-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="9920f-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="9920f-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9920f-119">De esta manera, esta función se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="9920f-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9920f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9920f-120">Requirements</span></span>



| <span data-ttu-id="9920f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9920f-121">Requirement</span></span> | <span data-ttu-id="9920f-122">Value</span><span class="sxs-lookup"><span data-stu-id="9920f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9920f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9920f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9920f-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9920f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9920f-125">Library</span></span><br/> | <dl> <span data-ttu-id="9920f-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9920f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9920f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9920f-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="9920f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
