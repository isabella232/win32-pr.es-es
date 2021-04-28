---
description: 'Función D3DXSphereBoundProbe (D3DX10math.h): determina si un rayo forma una intersección con el volumen del cuadro de límite de una esfera.'
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Función D3DXSphereBoundProbe (D3DX10math.h)
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
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108473"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="69cef-103">Función D3DXSphereBoundProbe (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="69cef-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="69cef-104">Determina si un rayo forma una intersección con el volumen del rectángulo delimitador de una esfera.</span><span class="sxs-lookup"><span data-stu-id="69cef-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="69cef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69cef-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="69cef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69cef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69cef-107">*pCenter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69cef-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69cef-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="69cef-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69cef-109">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la coordenada central de la esfera.</span><span class="sxs-lookup"><span data-stu-id="69cef-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="69cef-110">*Radio* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69cef-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69cef-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69cef-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69cef-112">Radio de la esfera.</span><span class="sxs-lookup"><span data-stu-id="69cef-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="69cef-113">*pRayPosition* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69cef-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69cef-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="69cef-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69cef-115">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la coordenada de origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="69cef-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="69cef-116">*pRayDirection* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69cef-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69cef-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="69cef-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69cef-118">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="69cef-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="69cef-119">Este vector no debe ser (0,0,0), pero no es necesario normalizarlo.</span><span class="sxs-lookup"><span data-stu-id="69cef-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69cef-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69cef-120">Return value</span></span>

<span data-ttu-id="69cef-121">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69cef-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69cef-122">Devuelve **TRUE** si el rayo forma una intersección con el volumen del cuadro de límite de la esfera.</span><span class="sxs-lookup"><span data-stu-id="69cef-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="69cef-123">De lo contrario, **devuelve FALSE.**</span><span class="sxs-lookup"><span data-stu-id="69cef-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="69cef-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69cef-124">Remarks</span></span>

<span data-ttu-id="69cef-125">**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo con la superficie de la esfera.</span><span class="sxs-lookup"><span data-stu-id="69cef-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cef-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69cef-126">Requirements</span></span>



| <span data-ttu-id="69cef-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="69cef-127">Requirement</span></span> | <span data-ttu-id="69cef-128">Value</span><span class="sxs-lookup"><span data-stu-id="69cef-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69cef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69cef-129">Header</span></span><br/>  | <dl> <span data-ttu-id="69cef-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="69cef-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="69cef-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69cef-131">Library</span></span><br/> | <dl> <span data-ttu-id="69cef-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="69cef-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69cef-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69cef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69cef-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="69cef-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
