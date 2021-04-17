---
description: La función D3DXBoxBoundProbe (D3DX10math. h) determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Función D3DXBoxBoundProbe (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187818"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="a3bbf-103">Función D3DXBoxBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="a3bbf-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="a3bbf-104">Determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bbf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3bbf-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="a3bbf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bbf-107">*pMin* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3bbf-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bbf-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3bbf-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3bbf-109">Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que describe la esquina inferior izquierda del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="a3bbf-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a3bbf-111">*pMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3bbf-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bbf-112">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3bbf-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3bbf-113">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina superior derecha del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="a3bbf-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a3bbf-115">*pRayPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3bbf-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bbf-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3bbf-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3bbf-117">Puntero a una estructura D3DXVECTOR3, que especifica la coordenada de origen del rayo.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="a3bbf-118">*pRayDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3bbf-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bbf-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3bbf-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3bbf-120">Puntero a una estructura D3DXVECTOR3, que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="a3bbf-121">Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3bbf-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3bbf-122">Return value</span></span>

<span data-ttu-id="a3bbf-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3bbf-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3bbf-124">Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="a3bbf-125">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3bbf-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3bbf-126">Remarks</span></span>

<span data-ttu-id="a3bbf-127">**D3DXBoxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro, no solo la superficie del cuadro.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="a3bbf-128">Los valores que se pasan a **D3DXBoxBoundProbe** son xmin, Xmax, YMIN, YMax, Zmin y Zmax.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="a3bbf-129">Por lo tanto, el siguiente código define las esquinas del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="a3bbf-130">La profundidad del cuadro de límite en la dirección z es Zmax-Zmin, en la dirección y es YMAX-YMIN y en la dirección x es XMax-xmin.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="a3bbf-131">Por ejemplo, con los siguientes vectores mínimo y máximo, min (-1,-1,-1) y Max (1, 1, 1), el cuadro de límite se define de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a3bbf-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3bbf-132">Requirements</span></span>



| <span data-ttu-id="a3bbf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3bbf-133">Requirement</span></span> | <span data-ttu-id="a3bbf-134">Value</span><span class="sxs-lookup"><span data-stu-id="a3bbf-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bbf-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3bbf-135">Header</span></span>  | <span data-ttu-id="a3bbf-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="a3bbf-136">D3DX10math.h</span></span> |
| <span data-ttu-id="a3bbf-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3bbf-137">Library</span></span> | <span data-ttu-id="a3bbf-138">D3DX10. lib</span><span class="sxs-lookup"><span data-stu-id="a3bbf-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="a3bbf-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3bbf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bbf-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="a3bbf-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
