---
description: Calcula el producto escalar de un plano y un vector 3D. Se supone que el parámetro w del vector es 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Función D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717553"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="fe736-104">D3DXPlaneDotNormal función)</span><span class="sxs-lookup"><span data-stu-id="fe736-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="fe736-105">Calcula el producto escalar de un plano y un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="fe736-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="fe736-106">Se supone que el parámetro w del vector es 0.</span><span class="sxs-lookup"><span data-stu-id="fe736-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe736-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe736-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="fe736-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe736-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe736-109">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe736-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe736-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe736-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fe736-111">Puntero a una estructura de [**D3DXPLANE**](d3dxplane.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fe736-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe736-112">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe736-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe736-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe736-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe736-114">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fe736-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe736-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe736-115">Return value</span></span>

<span data-ttu-id="fe736-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe736-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe736-117">Producto de punto del plano y Vector 3D.</span><span class="sxs-lookup"><span data-stu-id="fe736-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe736-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe736-118">Remarks</span></span>

<span data-ttu-id="fe736-119">Dado un plano (a, b, c, d) y un vector 3D (x, y, z), el valor devuelto de esta función es \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="fe736-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="fe736-120">La función **D3DXPlaneDotNormal** es útil para calcular el ángulo entre el normal del plano y otro normal.</span><span class="sxs-lookup"><span data-stu-id="fe736-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe736-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe736-121">Requirements</span></span>



| <span data-ttu-id="fe736-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe736-122">Requirement</span></span> | <span data-ttu-id="fe736-123">Value</span><span class="sxs-lookup"><span data-stu-id="fe736-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe736-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe736-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fe736-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe736-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe736-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe736-126">Library</span></span><br/> | <dl> <span data-ttu-id="fe736-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe736-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe736-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe736-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe736-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fe736-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fe736-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="fe736-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="fe736-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="fe736-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
