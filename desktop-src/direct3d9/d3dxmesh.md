---
description: 'Enumeración D3DXMESH: marcas que se usan para especificar las opciones de creación de una malla.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeración D3DXMESH (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098103"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="805f2-103">Enumeración D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="805f2-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="805f2-104">Marcas usadas para especificar opciones de creación para una malla.</span><span class="sxs-lookup"><span data-stu-id="805f2-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="805f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="805f2-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="805f2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="805f2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="805f2-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32BIT**</span><span class="sxs-lookup"><span data-stu-id="805f2-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-108">La malla tiene índices de 32 bits en lugar de índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="805f2-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="805f2-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="805f2-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="805f2-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-111">Use la [**marca de uso D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para los búferes de vértice e índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**PUNTOS D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="805f2-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-113">Use la [**marca de uso D3DUSAGE \_ POINTS para**](d3dusage.md) los búferes de vértice e índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="805f2-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-115">Use la [**marca de uso D3DUSAGE \_ RTPATCHES**](d3dusage.md) para los búferes de vértices e índices.</span><span class="sxs-lookup"><span data-stu-id="805f2-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="805f2-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-117">Al especificar esta marca, el vértice y el búfer de índice de la malla se crean con la marca [**D3DUSAGE \_ NPATCHES.**](d3dusage.md)</span><span class="sxs-lookup"><span data-stu-id="805f2-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="805f2-118">Esto es necesario si el objeto de malla se va a representar mediante la mejora de N revisiones mediante Direct3D.</span><span class="sxs-lookup"><span data-stu-id="805f2-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="805f2-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-120">Use la [**marca de uso D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ ADMINISTRADO**</span><span class="sxs-lookup"><span data-stu-id="805f2-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-122">Use la marca [**de uso D3DPOOL \_ MANAGED**](./d3dpool.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="805f2-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-124">Use la [**marca de uso \_ WRITEONLY de D3DUSAGE**](d3dusage.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="805f2-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-126">Use la [**marca de uso D3DUSAGE \_ DYNAMIC**](d3dusage.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="805f2-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-128">Use la [**marca de uso D3DUSAGE \_ SOFTWAREPROCESSING para**](d3dusage.md) los búferes de vértice.</span><span class="sxs-lookup"><span data-stu-id="805f2-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="805f2-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-130">Use la [**marca de uso \_ SYSTEMMEM de D3DPOOL**](./d3dpool.md) para búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ ADMINISTRADO**</span><span class="sxs-lookup"><span data-stu-id="805f2-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-132">Use la marca [**de uso D3DPOOL \_ MANAGED**](./d3dpool.md) para búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="805f2-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-134">Use la [**marca de uso \_ WRITEONLY de D3DUSAGE**](d3dusage.md) para búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="805f2-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-136">Use la marca de uso DYNAMIC de [**D3DUSAGE \_**](d3dusage.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="805f2-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-138">Use la [**marca de uso D3DUSAGE \_ SOFTWAREPROCESSING para**](d3dusage.md) los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="805f2-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**RECURSO COMPARTIDO DE VB D3DXMESH \_ \_**</span><span class="sxs-lookup"><span data-stu-id="805f2-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-140">Fuerza a las mallas clonadas a compartir búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="805f2-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-142">Use solo el procesamiento de hardware.</span><span class="sxs-lookup"><span data-stu-id="805f2-142">Use hardware processing only.</span></span> <span data-ttu-id="805f2-143">En el caso del dispositivo en modo mixto, esta marca hará que el sistema use hardware (si se admite en hardware) o que el procesamiento de software sea predeterminado.</span><span class="sxs-lookup"><span data-stu-id="805f2-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="805f2-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-145">Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="805f2-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ ADMINISTRADO**</span><span class="sxs-lookup"><span data-stu-id="805f2-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-147">Equivalente a especificar D3DXMESH \_ VB \_ MANAGED y D3DXMESH \_ IB \_ MANAGED.</span><span class="sxs-lookup"><span data-stu-id="805f2-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="805f2-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-149">Equivalente a especificar D3DXMESH \_ VB \_ WRITEONLY y D3DXMESH \_ IB \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="805f2-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="805f2-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-151">Equivalente a especificar D3DXMESH \_ VB \_ DYNAMIC y D3DXMESH \_ IB \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="805f2-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="805f2-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="805f2-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="805f2-153">Equivalente a especificar D3DXMESH \_ VB \_ SOFTWAREPROCESSING y D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="805f2-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="805f2-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="805f2-154">Remarks</span></span>

<span data-ttu-id="805f2-155">Una malla de 32 bits (D3DXMESH de 32 BITS) puede admitir teóricamente \_ (2^32)-1 caras y vértices.</span><span class="sxs-lookup"><span data-stu-id="805f2-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="805f2-156">Sin embargo, no es práctico asignar memoria para una malla de gran tamaño en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="805f2-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="805f2-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805f2-157">Requirements</span></span>



| <span data-ttu-id="805f2-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="805f2-158">Requirement</span></span> | <span data-ttu-id="805f2-159">Value</span><span class="sxs-lookup"><span data-stu-id="805f2-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="805f2-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="805f2-160">Header</span></span><br/> | <dl> <span data-ttu-id="805f2-161"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="805f2-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805f2-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="805f2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805f2-163">Enumeraciones D3DX</span><span class="sxs-lookup"><span data-stu-id="805f2-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
