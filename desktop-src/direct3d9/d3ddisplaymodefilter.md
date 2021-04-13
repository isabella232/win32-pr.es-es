---
description: Especifica los tipos de modos de presentación que se van a filtrar.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Estructura D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362492"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="12a38-103">Estructura D3DDISPLAYMODEFILTER</span><span class="sxs-lookup"><span data-stu-id="12a38-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="12a38-104">Especifica los tipos de modos de presentación que se van a filtrar.</span><span class="sxs-lookup"><span data-stu-id="12a38-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12a38-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="12a38-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="12a38-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12a38-107">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="12a38-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="12a38-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12a38-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12a38-109">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="12a38-109">The size of this structure.</span></span> <span data-ttu-id="12a38-110">Siempre debe establecerse en sizeof (D3DDISPLAYMODEFILTER).</span><span class="sxs-lookup"><span data-stu-id="12a38-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="12a38-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="12a38-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="12a38-112">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="12a38-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12a38-113">Formato del modo de presentación que se va a filtrar. Vea [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="12a38-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="12a38-114">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="12a38-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="12a38-115">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="12a38-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12a38-116">Indica si el orden Scanline es entrelazado o progresivo.</span><span class="sxs-lookup"><span data-stu-id="12a38-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="12a38-117">Vea [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="12a38-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12a38-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12a38-118">Requirements</span></span>



| <span data-ttu-id="12a38-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="12a38-119">Requirement</span></span> | <span data-ttu-id="12a38-120">Value</span><span class="sxs-lookup"><span data-stu-id="12a38-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12a38-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12a38-121">Header</span></span><br/> | <dl> <span data-ttu-id="12a38-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a38-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a38-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="12a38-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a38-124">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="12a38-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
