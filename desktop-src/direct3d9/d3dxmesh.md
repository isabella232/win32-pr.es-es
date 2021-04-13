---
description: Marcas que se usan para especificar las opciones de creación de una malla.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeración D3DXMESH (D3dx9mesh. h)
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
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362436"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="bce55-103">Enumeración D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="bce55-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="bce55-104">Marcas que se usan para especificar las opciones de creación de una malla.</span><span class="sxs-lookup"><span data-stu-id="bce55-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bce55-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="bce55-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bce55-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bce55-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 bits**</span><span class="sxs-lookup"><span data-stu-id="bce55-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-108">La malla tiene índices de 32 bits en lugar de índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bce55-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="bce55-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="bce55-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="bce55-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-111">Use la marca de uso de [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="bce55-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**\_Puntos D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="bce55-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-113">Use la marca de uso de [**\_ puntos D3DUSAGE**](d3dusage.md) para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="bce55-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="bce55-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-115">Use la marca de uso de [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="bce55-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="bce55-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-117">Si se especifica esta marca, el vértice y el búfer de índice de la malla se crearán con la marca [**D3DUSAGE \_ NPATCHES**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="bce55-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="bce55-118">Esto es necesario si el objeto de malla se va a representar mediante la mejora de N-patch mediante Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bce55-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="bce55-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-120">Use la marca de uso de [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ administrado**</span><span class="sxs-lookup"><span data-stu-id="bce55-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-122">Use la marca de uso [**\_ administrado D3DPOOL**](./d3dpool.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="bce55-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-124">Use la marca de uso [**\_ WRITEONLY de D3DUSAGE**](d3dusage.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dinámico**</span><span class="sxs-lookup"><span data-stu-id="bce55-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-126">Use la marca de uso [**\_ dinámico D3DUSAGE**](d3dusage.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="bce55-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-128">Use la marca de uso de [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="bce55-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-130">Use la marca de uso [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bce55-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**Administrado por D3DXMESH \_ IB \_**</span><span class="sxs-lookup"><span data-stu-id="bce55-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-132">Use la marca de uso [**\_ administrado D3DPOOL**](./d3dpool.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bce55-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="bce55-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-134">Use la marca de uso [**\_ WRITEONLY de D3DUSAGE**](d3dusage.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bce55-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ Dynamic**</span><span class="sxs-lookup"><span data-stu-id="bce55-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-136">Use la marca de uso [**\_ dinámico D3DUSAGE**](d3dusage.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bce55-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="bce55-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-138">Use la marca de uso [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bce55-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Recurso compartido de VB D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="bce55-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-140">Obliga a que las mallas clonadas compartan búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="bce55-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-142">Usar solo el procesamiento de hardware.</span><span class="sxs-lookup"><span data-stu-id="bce55-142">Use hardware processing only.</span></span> <span data-ttu-id="bce55-143">En el caso de dispositivos de modo mixto, esta marca hará que el sistema use el hardware (si se admite en el hardware) o el procesamiento de software de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bce55-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="bce55-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-145">Equivale a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="bce55-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**Administrado por D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="bce55-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-147">Equivale a especificar D3DXMESH \_ VB \_ administrado y D3DXMESH \_ IB \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="bce55-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="bce55-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-149">Equivalente a especificar tanto D3DXMESH \_ VB \_ WRITEONLY como D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="bce55-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dinámico**</span><span class="sxs-lookup"><span data-stu-id="bce55-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-151">Equivale a especificar D3DXMESH \_ VB \_ Dynamic y D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="bce55-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="bce55-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="bce55-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="bce55-153">Equivale a especificar D3DXMESH \_ VB \_ SOFTWAREPROCESSING y D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="bce55-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bce55-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce55-154">Remarks</span></span>

<span data-ttu-id="bce55-155">Una malla de 32 bits (D3DXMESH \_ 32 bits) puede admitir teóricamente (2 ^ 32)-1 caras y vértices.</span><span class="sxs-lookup"><span data-stu-id="bce55-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="bce55-156">Sin embargo, la asignación de memoria para una malla que es grande en un sistema operativo de 32 bits no es práctica.</span><span class="sxs-lookup"><span data-stu-id="bce55-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce55-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce55-157">Requirements</span></span>



| <span data-ttu-id="bce55-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce55-158">Requirement</span></span> | <span data-ttu-id="bce55-159">Value</span><span class="sxs-lookup"><span data-stu-id="bce55-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce55-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bce55-160">Header</span></span><br/> | <dl> <span data-ttu-id="bce55-161"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce55-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce55-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce55-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce55-163">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="bce55-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
