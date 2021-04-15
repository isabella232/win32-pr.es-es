---
description: Describe una revisión de orden superior rectangular.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707925"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="8d2d8-103">Estructura de información de D3DRECTPATCH \_</span><span class="sxs-lookup"><span data-stu-id="8d2d8-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="8d2d8-104">Describe una revisión de orden superior rectangular.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d2d8-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="8d2d8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d2d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d2d8-107">**StartVertexOffsetWidth**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-109">Ancho de desplazamiento de vértice inicial, en número de vértices.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d8-110">**StartVertexOffsetHeight**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-112">Alto de desplazamiento de vértice inicial, en número de vértices.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d8-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-115">Ancho de cada vértice, en número de vértices.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d8-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-118">Alto de cada vértice, en número de vértices.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d8-119">**STRI**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-121">Ancho de la matriz de vértices bidimensional imaginario, que ocupa el mismo espacio que el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="8d2d8-122">Para obtener un ejemplo, vea el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d8-123">**Basis**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-124">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-125">Miembro del tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define el tipo base para la revisión de orden superior rectangular.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="8d2d8-126">Value</span><span class="sxs-lookup"><span data-stu-id="8d2d8-126">Value</span></span>                 | <span data-ttu-id="8d2d8-127">Pedido admitido</span><span class="sxs-lookup"><span data-stu-id="8d2d8-127">Order supported</span></span>            | <span data-ttu-id="8d2d8-128">Ancho y alto</span><span class="sxs-lookup"><span data-stu-id="8d2d8-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="8d2d8-129">D3DBASIS \_ Bézier</span><span class="sxs-lookup"><span data-stu-id="8d2d8-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="8d2d8-130">Lineal, cúbica y quinta</span><span class="sxs-lookup"><span data-stu-id="8d2d8-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="8d2d8-131">Width = Height = (DWORD) Order + 1</span><span class="sxs-lookup"><span data-stu-id="8d2d8-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="8d2d8-132">D3DBASIS \_ BSPLINE</span><span class="sxs-lookup"><span data-stu-id="8d2d8-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="8d2d8-133">Lineal, cúbica y quinta</span><span class="sxs-lookup"><span data-stu-id="8d2d8-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="8d2d8-134">Ancho = orden de > de altura (DWORD)</span><span class="sxs-lookup"><span data-stu-id="8d2d8-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="8d2d8-135">D3DBASIS \_ interpolación</span><span class="sxs-lookup"><span data-stu-id="8d2d8-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="8d2d8-136">Cúbica</span><span class="sxs-lookup"><span data-stu-id="8d2d8-136">Cubic</span></span>                      | <span data-ttu-id="8d2d8-137">Ancho = orden de > de altura (DWORD)</span><span class="sxs-lookup"><span data-stu-id="8d2d8-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8d2d8-138">**Grado**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="8d2d8-139">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d2d8-140">Miembro del tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , que define el grado de la revisión rectangular.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d2d8-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d2d8-141">Remarks</span></span>

<span data-ttu-id="8d2d8-142">En el diagrama siguiente se identifican los parámetros que especifican una revisión de rectángulo.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![diagrama de una revisión rectangular de orden superior y los parámetros que lo especifican](images/hop-rectpatch.png)

<span data-ttu-id="8d2d8-144">Cada uno de los vértices del búfer de vértices se muestra como un punto negro.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="8d2d8-145">En este caso, el búfer de vértices tiene 20 vértices en él, 16 de los cuales se encuentran en la revisión del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="8d2d8-146">STRIDE es el número de vértices en el ancho del búfer de vértices, en este caso cinco.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="8d2d8-147">El desplazamiento x al primer vértice se denomina StartIndexVertexWidth y en este caso 1.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="8d2d8-148">El desplazamiento y al primer vértice de la revisión se denomina StartIndexVertexHeight y, en este caso, 0.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="8d2d8-149">Para representar una secuencia de revisiones rectangulares individuales (sin mosaico), debe interpretar la geometría como una revisión rectangular larga (1 x N) rectangular.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="8d2d8-150">La estructura de **\_ información de D3DRECTPATCH** para esta franja (Bézier cúbica) se configuraría de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="8d2d8-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="8d2d8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d2d8-151">Requirements</span></span>



| <span data-ttu-id="8d2d8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d2d8-152">Requirement</span></span> | <span data-ttu-id="8d2d8-153">Value</span><span class="sxs-lookup"><span data-stu-id="8d2d8-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d2d8-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d2d8-154">Header</span></span><br/> | <dl> <span data-ttu-id="8d2d8-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d2d8-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d2d8-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d2d8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2d8-157">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8d2d8-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="8d2d8-158">**DrawRectPatch**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="8d2d8-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="8d2d8-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
