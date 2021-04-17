---
description: Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Función D3DXSphereBoundProbe (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678789"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="91788-103">Función D3DXSphereBoundProbe (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="91788-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="91788-104">Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.</span><span class="sxs-lookup"><span data-stu-id="91788-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="91788-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91788-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="91788-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91788-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91788-107">*pCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91788-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91788-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="91788-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="91788-109">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la coordenada central de la esfera.</span><span class="sxs-lookup"><span data-stu-id="91788-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="91788-110">*RADIUS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91788-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91788-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91788-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91788-112">Radio de la esfera.</span><span class="sxs-lookup"><span data-stu-id="91788-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="91788-113">*pRayPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91788-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91788-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="91788-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="91788-115">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la coordenada de origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="91788-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="91788-116">*pRayDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91788-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91788-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="91788-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="91788-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="91788-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="91788-119">Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.</span><span class="sxs-lookup"><span data-stu-id="91788-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91788-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91788-120">Return value</span></span>

<span data-ttu-id="91788-121">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91788-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91788-122">Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera.</span><span class="sxs-lookup"><span data-stu-id="91788-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="91788-123">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="91788-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="91788-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91788-124">Remarks</span></span>

<span data-ttu-id="91788-125">**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo la superficie de la esfera.</span><span class="sxs-lookup"><span data-stu-id="91788-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="91788-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91788-126">Requirements</span></span>



| <span data-ttu-id="91788-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="91788-127">Requirement</span></span> | <span data-ttu-id="91788-128">Value</span><span class="sxs-lookup"><span data-stu-id="91788-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91788-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91788-129">Header</span></span><br/>  | <dl> <span data-ttu-id="91788-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="91788-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="91788-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91788-131">Library</span></span><br/> | <dl> <span data-ttu-id="91788-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91788-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91788-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="91788-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91788-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="91788-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
