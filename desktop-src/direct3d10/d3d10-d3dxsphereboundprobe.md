---
description: Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Función D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821335"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="17e63-103">Función D3DXSphereBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="17e63-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="17e63-104">Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.</span><span class="sxs-lookup"><span data-stu-id="17e63-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17e63-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="17e63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e63-107">*pCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17e63-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="17e63-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="17e63-109">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la coordenada central de la esfera.</span><span class="sxs-lookup"><span data-stu-id="17e63-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="17e63-110">*RADIUS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17e63-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17e63-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17e63-112">Radio de la esfera.</span><span class="sxs-lookup"><span data-stu-id="17e63-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="17e63-113">*pRayPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17e63-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="17e63-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="17e63-115">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la coordenada de origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="17e63-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="17e63-116">*pRayDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17e63-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="17e63-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="17e63-118">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="17e63-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="17e63-119">Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.</span><span class="sxs-lookup"><span data-stu-id="17e63-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e63-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17e63-120">Return value</span></span>

<span data-ttu-id="17e63-121">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17e63-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17e63-122">Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera.</span><span class="sxs-lookup"><span data-stu-id="17e63-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="17e63-123">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="17e63-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e63-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17e63-124">Remarks</span></span>

<span data-ttu-id="17e63-125">**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo la superficie de la esfera.</span><span class="sxs-lookup"><span data-stu-id="17e63-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e63-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e63-126">Requirements</span></span>



| <span data-ttu-id="17e63-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e63-127">Requirement</span></span> | <span data-ttu-id="17e63-128">Value</span><span class="sxs-lookup"><span data-stu-id="17e63-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17e63-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17e63-129">Header</span></span><br/>  | <dl> <span data-ttu-id="17e63-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e63-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="17e63-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17e63-131">Library</span></span><br/> | <dl> <span data-ttu-id="17e63-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17e63-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17e63-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="17e63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e63-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="17e63-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
