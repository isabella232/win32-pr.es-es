---
description: Información acerca de las propiedades de un modo de presentación.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Estructura D3DDISPLAYMODEEX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698211"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="f8156-103">Estructura D3DDISPLAYMODEEX</span><span class="sxs-lookup"><span data-stu-id="f8156-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="f8156-104">Información acerca de las propiedades de un modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f8156-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8156-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8156-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="f8156-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8156-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8156-107">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="f8156-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-109">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="f8156-109">The size of this structure.</span></span> <span data-ttu-id="f8156-110">Siempre debe establecerse en sizeof (D3DDISPLAYMODEEX).</span><span class="sxs-lookup"><span data-stu-id="f8156-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="f8156-111">**Width**</span><span class="sxs-lookup"><span data-stu-id="f8156-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-113">Ancho del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f8156-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="f8156-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="f8156-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-116">Alto del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f8156-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="f8156-117">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="f8156-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-119">Frecuencia de actualización del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f8156-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="f8156-120">**Format**</span><span class="sxs-lookup"><span data-stu-id="f8156-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-121">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-122">Formato del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f8156-122">Format of the display mode.</span></span> <span data-ttu-id="f8156-123">Vea [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="f8156-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8156-124">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="f8156-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="f8156-125">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="f8156-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8156-126">Indica si el orden Scanline es progresivo o entrelazado.</span><span class="sxs-lookup"><span data-stu-id="f8156-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="f8156-127">Vea [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="f8156-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8156-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8156-128">Remarks</span></span>

<span data-ttu-id="f8156-129">Esta estructura se usa en varios métodos para crear y administrar dispositivos 9Ex de Direct3D ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) y intercambio ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span><span class="sxs-lookup"><span data-stu-id="f8156-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8156-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8156-130">Requirements</span></span>



| <span data-ttu-id="f8156-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8156-131">Requirement</span></span> | <span data-ttu-id="f8156-132">Value</span><span class="sxs-lookup"><span data-stu-id="f8156-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8156-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8156-133">Header</span></span><br/> | <dl> <span data-ttu-id="f8156-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8156-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8156-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8156-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8156-136">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="f8156-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
