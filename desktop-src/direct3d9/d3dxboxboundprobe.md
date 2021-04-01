---
description: Determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Función D3DXBoxBoundProbe (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157200"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="19ca6-103">D3DXBoxBoundProbe función)</span><span class="sxs-lookup"><span data-stu-id="19ca6-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="19ca6-104">Determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.</span><span class="sxs-lookup"><span data-stu-id="19ca6-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ca6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19ca6-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="19ca6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19ca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ca6-107">*pMin* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19ca6-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ca6-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19ca6-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="19ca6-109">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina inferior izquierda del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="19ca6-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="19ca6-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="19ca6-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19ca6-111">*pMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19ca6-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ca6-112">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19ca6-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="19ca6-113">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina superior derecha del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="19ca6-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="19ca6-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="19ca6-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19ca6-115">*pRayPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19ca6-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ca6-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19ca6-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="19ca6-117">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la coordenada de origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="19ca6-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="19ca6-118">*pRayDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19ca6-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ca6-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19ca6-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="19ca6-120">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="19ca6-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="19ca6-121">Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.</span><span class="sxs-lookup"><span data-stu-id="19ca6-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ca6-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19ca6-122">Return value</span></span>

<span data-ttu-id="19ca6-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19ca6-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19ca6-124">Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro.</span><span class="sxs-lookup"><span data-stu-id="19ca6-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="19ca6-125">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="19ca6-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ca6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ca6-126">Remarks</span></span>

<span data-ttu-id="19ca6-127">**D3DXboxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro, no solo la superficie del cuadro.</span><span class="sxs-lookup"><span data-stu-id="19ca6-127">**D3DXboxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="19ca6-128">Los valores que se pasan a **D3DXboxBoundProbe** son xmin, Xmax, YMIN, YMax, Zmin y Zmax.</span><span class="sxs-lookup"><span data-stu-id="19ca6-128">The values passed to **D3DXboxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="19ca6-129">Por lo tanto, el siguiente código define las esquinas del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="19ca6-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="19ca6-130">La profundidad del cuadro de límite en la dirección z es Zmax-Zmin, en la dirección y es YMAX-YMIN y en la dirección x es XMax-xmin.</span><span class="sxs-lookup"><span data-stu-id="19ca6-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="19ca6-131">Por ejemplo, con los siguientes vectores mínimo y máximo, min (-1,-1,-1) y Max (1, 1, 1), el cuadro de límite se define de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="19ca6-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="19ca6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ca6-132">Requirements</span></span>



| <span data-ttu-id="19ca6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ca6-133">Requirement</span></span> | <span data-ttu-id="19ca6-134">Value</span><span class="sxs-lookup"><span data-stu-id="19ca6-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19ca6-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19ca6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="19ca6-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ca6-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19ca6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19ca6-137">Library</span></span><br/> | <dl> <span data-ttu-id="19ca6-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19ca6-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19ca6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ca6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ca6-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="19ca6-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="19ca6-141">**D3DXComputeBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="19ca6-141">**D3DXComputeBoundingBox**</span></span>](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
