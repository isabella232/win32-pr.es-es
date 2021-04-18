---
description: Describe una revisión de orden superior triangular.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718398"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="163f4-103">Estructura de información de D3DTRIPATCH \_</span><span class="sxs-lookup"><span data-stu-id="163f4-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="163f4-104">Describe una revisión de orden superior triangular.</span><span class="sxs-lookup"><span data-stu-id="163f4-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="163f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="163f4-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="163f4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="163f4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="163f4-107">**StartVertexOffset**</span><span class="sxs-lookup"><span data-stu-id="163f4-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="163f4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="163f4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="163f4-109">Desplazamiento de vértice inicial, en número de vértices.</span><span class="sxs-lookup"><span data-stu-id="163f4-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="163f4-110">**NumVertices**</span><span class="sxs-lookup"><span data-stu-id="163f4-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="163f4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="163f4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="163f4-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="163f4-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="163f4-113">**Basis**</span><span class="sxs-lookup"><span data-stu-id="163f4-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="163f4-114">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="163f4-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="163f4-115">Miembro del tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define el tipo base para la revisión de orden superior triangular.</span><span class="sxs-lookup"><span data-stu-id="163f4-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="163f4-116">El único valor válido para este miembro es D3DBASIS \_ Bézier.</span><span class="sxs-lookup"><span data-stu-id="163f4-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="163f4-117">**Grado**</span><span class="sxs-lookup"><span data-stu-id="163f4-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="163f4-118">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="163f4-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="163f4-119">Miembro del tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , que define el tipo de grado de la revisión de orden superior triangular.</span><span class="sxs-lookup"><span data-stu-id="163f4-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="163f4-120">Value</span><span class="sxs-lookup"><span data-stu-id="163f4-120">Value</span></span>                | <span data-ttu-id="163f4-121">Número de vértices</span><span class="sxs-lookup"><span data-stu-id="163f4-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="163f4-122">D3DDEGREE \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="163f4-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="163f4-123">10</span><span class="sxs-lookup"><span data-stu-id="163f4-123">10</span></span>                 |
| <span data-ttu-id="163f4-124">\_Lineal D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="163f4-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="163f4-125">3</span><span class="sxs-lookup"><span data-stu-id="163f4-125">3</span></span>                  |
| <span data-ttu-id="163f4-126">D3DDEGREE \_ cuadrático</span><span class="sxs-lookup"><span data-stu-id="163f4-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="163f4-127">N/D</span><span class="sxs-lookup"><span data-stu-id="163f4-127">N/A</span></span>                |
| <span data-ttu-id="163f4-128">D3DDEGREE \_ quintal</span><span class="sxs-lookup"><span data-stu-id="163f4-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="163f4-129">21</span><span class="sxs-lookup"><span data-stu-id="163f4-129">21</span></span>                 |



 

<span data-ttu-id="163f4-130">N/A: no disponible.</span><span class="sxs-lookup"><span data-stu-id="163f4-130">N/A - Not available.</span></span> <span data-ttu-id="163f4-131">No se admite.</span><span class="sxs-lookup"><span data-stu-id="163f4-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="163f4-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="163f4-132">Remarks</span></span>

<span data-ttu-id="163f4-133">Por ejemplo, el diagrama siguiente identifica el orden de los vértices y los números de segmento para una revisión de triángulo Bézier cúbica.</span><span class="sxs-lookup"><span data-stu-id="163f4-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="163f4-134">El orden de los vértices determina los números de segmento usados por [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span><span class="sxs-lookup"><span data-stu-id="163f4-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="163f4-135">El desplazamiento es el número de bytes al primer vértice de la revisión del triángulo en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="163f4-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![diagrama de una revisión de orden superior triangular con nueve vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="163f4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="163f4-137">Requirements</span></span>



| <span data-ttu-id="163f4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="163f4-138">Requirement</span></span> | <span data-ttu-id="163f4-139">Value</span><span class="sxs-lookup"><span data-stu-id="163f4-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="163f4-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="163f4-140">Header</span></span><br/> | <dl> <span data-ttu-id="163f4-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="163f4-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="163f4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="163f4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="163f4-143">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="163f4-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="163f4-144">**DrawTriPatch**</span><span class="sxs-lookup"><span data-stu-id="163f4-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="163f4-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="163f4-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
