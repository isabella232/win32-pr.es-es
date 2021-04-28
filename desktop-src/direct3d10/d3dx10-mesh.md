---
description: 'D3DX10_MESH enumeración: marcas usadas para especificar opciones de creación para una malla.'
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH enumeración (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105443"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="0d49d-103">D3DX10 \_ MESH (enumeración)</span><span class="sxs-lookup"><span data-stu-id="0d49d-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="0d49d-104">Marcas usadas para especificar opciones de creación para una malla.</span><span class="sxs-lookup"><span data-stu-id="0d49d-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d49d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d49d-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="0d49d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0d49d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0d49d-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ DE 32 \_ BITS**</span><span class="sxs-lookup"><span data-stu-id="0d49d-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="0d49d-108">La malla tiene índices de 32 bits en lugar de índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0d49d-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="0d49d-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0d49d-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0d49d-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**ADYACENCIA \_ DE \_ GS DE D3DX10 MESH \_**</span><span class="sxs-lookup"><span data-stu-id="0d49d-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="0d49d-111">Indica que la malla contiene datos de adyacencia del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0d49d-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d49d-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d49d-112">Remarks</span></span>

<span data-ttu-id="0d49d-113">Una malla de 32 bits (D3DXMESH de 32 BITS) puede admitir teóricamente \_ (2):1 caras y vértices.</span><span class="sxs-lookup"><span data-stu-id="0d49d-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="0d49d-114">Sin embargo, no es práctico asignar memoria para una malla que sea grande en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0d49d-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d49d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d49d-115">Requirements</span></span>



| <span data-ttu-id="0d49d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d49d-116">Requirement</span></span> | <span data-ttu-id="0d49d-117">Value</span><span class="sxs-lookup"><span data-stu-id="0d49d-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d49d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d49d-118">Header</span></span><br/> | <dl> <span data-ttu-id="0d49d-119"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="0d49d-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d49d-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d49d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d49d-121">Enumeraciones D3DX</span><span class="sxs-lookup"><span data-stu-id="0d49d-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




