---
description: Calcula el producto escalar de un plano y un vector 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Función D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717558"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="21258-103">D3DXPlaneDot función)</span><span class="sxs-lookup"><span data-stu-id="21258-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="21258-104">Calcula el producto escalar de un plano y un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="21258-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="21258-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21258-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="21258-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21258-107">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21258-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21258-108">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="21258-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="21258-109">Puntero a una estructura de [**D3DXPLANE**](d3dxplane.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="21258-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="21258-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21258-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21258-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="21258-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="21258-112">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="21258-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21258-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21258-113">Return value</span></span>

<span data-ttu-id="21258-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21258-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21258-115">Producto de punto del plano y el vector 4D.</span><span class="sxs-lookup"><span data-stu-id="21258-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="21258-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21258-116">Remarks</span></span>

<span data-ttu-id="21258-117">Dado un plano (a, b, c, d) y un vector 4D (x, y, z, w), el valor devuelto de esta función es \* x + b \* y + c \* z + d \* w.</span><span class="sxs-lookup"><span data-stu-id="21258-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="21258-118">La función **D3DXPlaneDot** es útil para determinar la relación del plano con una coordenada homogénea.</span><span class="sxs-lookup"><span data-stu-id="21258-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="21258-119">Por ejemplo, esta función se puede usar para determinar si una coordenada determinada está en un plano determinado o en qué lado de un plano determinado se encuentra una coordenada determinada.</span><span class="sxs-lookup"><span data-stu-id="21258-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="21258-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21258-120">Requirements</span></span>



| <span data-ttu-id="21258-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21258-121">Requirement</span></span> | <span data-ttu-id="21258-122">Value</span><span class="sxs-lookup"><span data-stu-id="21258-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21258-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21258-123">Header</span></span><br/>  | <dl> <span data-ttu-id="21258-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="21258-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="21258-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21258-125">Library</span></span><br/> | <dl> <span data-ttu-id="21258-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21258-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21258-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="21258-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21258-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="21258-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="21258-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="21258-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="21258-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="21258-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
