---
description: Estructura que contiene los atributos de una malla de revisión.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Estructura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362428"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="9dee4-103">Estructura D3DXPATCHINFO</span><span class="sxs-lookup"><span data-stu-id="9dee4-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="9dee4-104">Estructura que contiene los atributos de una malla de revisión.</span><span class="sxs-lookup"><span data-stu-id="9dee4-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dee4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dee4-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="9dee4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9dee4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9dee4-107">**PatchType**</span><span class="sxs-lookup"><span data-stu-id="9dee4-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="9dee4-108">Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="9dee4-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9dee4-109">Tipo de revisión.</span><span class="sxs-lookup"><span data-stu-id="9dee4-109">The patch type.</span></span> <span data-ttu-id="9dee4-110">Para obtener información sobre los tipos de revisión, vea [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="9dee4-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dee4-111">**Grado**</span><span class="sxs-lookup"><span data-stu-id="9dee4-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="9dee4-112">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="9dee4-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9dee4-113">Grado de las curvas utilizadas para construir la revisión.</span><span class="sxs-lookup"><span data-stu-id="9dee4-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="9dee4-114">Para obtener información acerca de los grados admitidos, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="9dee4-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dee4-115">**Basis**</span><span class="sxs-lookup"><span data-stu-id="9dee4-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="9dee4-116">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="9dee4-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9dee4-117">Tipo de curva que se usa para construir la revisión.</span><span class="sxs-lookup"><span data-stu-id="9dee4-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="9dee4-118">Para obtener información sobre los tipos de base admitidos, vea [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="9dee4-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dee4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dee4-119">Remarks</span></span>

<span data-ttu-id="9dee4-120">Una malla es un conjunto de caras, cada una de las cuales se describe mediante un polígono simple.</span><span class="sxs-lookup"><span data-stu-id="9dee4-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="9dee4-121">Los objetos se pueden crear conectando varias mallas juntas.</span><span class="sxs-lookup"><span data-stu-id="9dee4-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="9dee4-122">Una malla de revisión se construye a partir de revisiones.</span><span class="sxs-lookup"><span data-stu-id="9dee4-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="9dee4-123">Una revisión es una pieza de cuatro caras de geometría construida a partir de curvas.</span><span class="sxs-lookup"><span data-stu-id="9dee4-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="9dee4-124">El tipo de curva que se usa y el orden de la curva pueden ser variados para que la superficie de la revisión quepa prácticamente cualquier forma de superficie.</span><span class="sxs-lookup"><span data-stu-id="9dee4-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="9dee4-125">Se admiten los siguientes tipos de combinaciones de revisiones:</span><span class="sxs-lookup"><span data-stu-id="9dee4-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="9dee4-126">Tipo de revisión</span><span class="sxs-lookup"><span data-stu-id="9dee4-126">Patch Type</span></span> | <span data-ttu-id="9dee4-127">Basis</span><span class="sxs-lookup"><span data-stu-id="9dee4-127">Basis</span></span>       | <span data-ttu-id="9dee4-128">Grado</span><span class="sxs-lookup"><span data-stu-id="9dee4-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="9dee4-129">Rectángulo</span><span class="sxs-lookup"><span data-stu-id="9dee4-129">Rectangle</span></span>  | <span data-ttu-id="9dee4-130">Bézier</span><span class="sxs-lookup"><span data-stu-id="9dee4-130">Bezier</span></span>      | <span data-ttu-id="9dee4-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="9dee4-131">2,3,5</span></span>  |
| <span data-ttu-id="9dee4-132">Rectángulo</span><span class="sxs-lookup"><span data-stu-id="9dee4-132">Rectangle</span></span>  | <span data-ttu-id="9dee4-133">Spline B</span><span class="sxs-lookup"><span data-stu-id="9dee4-133">B-Spline</span></span>    | <span data-ttu-id="9dee4-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="9dee4-134">2,3,5</span></span>  |
| <span data-ttu-id="9dee4-135">Rectángulo</span><span class="sxs-lookup"><span data-stu-id="9dee4-135">Rectangle</span></span>  | <span data-ttu-id="9dee4-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="9dee4-136">Catmull-Rom</span></span> | <span data-ttu-id="9dee4-137">3</span><span class="sxs-lookup"><span data-stu-id="9dee4-137">3</span></span>      |
| <span data-ttu-id="9dee4-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="9dee4-138">Triangle</span></span>   | <span data-ttu-id="9dee4-139">Bézier</span><span class="sxs-lookup"><span data-stu-id="9dee4-139">Bezier</span></span>      | <span data-ttu-id="9dee4-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="9dee4-140">2,3,5</span></span>  |
| <span data-ttu-id="9dee4-141">N-patch</span><span class="sxs-lookup"><span data-stu-id="9dee4-141">N-patch</span></span>    | <span data-ttu-id="9dee4-142">N/D</span><span class="sxs-lookup"><span data-stu-id="9dee4-142">N/A</span></span>         | <span data-ttu-id="9dee4-143">3</span><span class="sxs-lookup"><span data-stu-id="9dee4-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="9dee4-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dee4-144">Requirements</span></span>



| <span data-ttu-id="9dee4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dee4-145">Requirement</span></span> | <span data-ttu-id="9dee4-146">Value</span><span class="sxs-lookup"><span data-stu-id="9dee4-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dee4-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dee4-147">Header</span></span><br/> | <dl> <span data-ttu-id="9dee4-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dee4-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dee4-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dee4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dee4-150">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="9dee4-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="9dee4-151">**Información de D3DRECTPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="9dee4-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="9dee4-152">**Información de D3DTRIPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="9dee4-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="9dee4-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="9dee4-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
