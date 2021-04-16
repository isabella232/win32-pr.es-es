---
description: Escalar el plano con el factor de escala especificado.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: Función D3DXPlaneScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678769"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="16851-103">D3DXPlaneScale función)</span><span class="sxs-lookup"><span data-stu-id="16851-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="16851-104">Escalar el plano con el factor de escala especificado.</span><span class="sxs-lookup"><span data-stu-id="16851-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="16851-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16851-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="16851-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16851-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16851-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16851-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16851-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="16851-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="16851-109">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="16851-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16851-110">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16851-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16851-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="16851-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="16851-112">Puntero a la estructura de [**D3DXPLANE**](d3dxplane.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="16851-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16851-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="16851-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16851-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16851-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16851-115">Factor de escala.</span><span class="sxs-lookup"><span data-stu-id="16851-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16851-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16851-116">Return value</span></span>

<span data-ttu-id="16851-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="16851-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="16851-118">Puntero a una estructura [**D3DXPLANE**](d3dxplane.md) que representa el plano escalado.</span><span class="sxs-lookup"><span data-stu-id="16851-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="16851-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16851-119">Remarks</span></span>

<span data-ttu-id="16851-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="16851-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="16851-121">Por lo tanto, esta función se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="16851-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16851-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16851-122">Requirements</span></span>



| <span data-ttu-id="16851-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16851-123">Requirement</span></span> | <span data-ttu-id="16851-124">Value</span><span class="sxs-lookup"><span data-stu-id="16851-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16851-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16851-125">Header</span></span><br/>  | <dl> <span data-ttu-id="16851-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16851-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="16851-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16851-127">Library</span></span><br/> | <dl> <span data-ttu-id="16851-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16851-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16851-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="16851-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16851-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="16851-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
