---
description: Describe una superficie de representación.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC estructura (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003807"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="0ab8a-103">D3DXRTS \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="0ab8a-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="0ab8a-104">Describe una superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ab8a-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="0ab8a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ab8a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ab8a-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="0ab8a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ab8a-109">Ancho de la superficie de representación, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8a-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="0ab8a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ab8a-112">Alto de la superficie de representación, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8a-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="0ab8a-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ab8a-115">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8a-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="0ab8a-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ab8a-118">Si **es true**, la superficie de representación admite una superficie de estarcido de profundidad; de lo contrario, este miembro se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8a-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0ab8a-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0ab8a-121">Si DepthStencil se establece en **true**, este parámetro es un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de la galería de símbolos de profundidad de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0ab8a-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ab8a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ab8a-122">Requirements</span></span>



| <span data-ttu-id="0ab8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ab8a-123">Requirement</span></span> | <span data-ttu-id="0ab8a-124">Value</span><span class="sxs-lookup"><span data-stu-id="0ab8a-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab8a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ab8a-125">Header</span></span><br/> | <dl> <span data-ttu-id="0ab8a-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8a-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ab8a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ab8a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab8a-128">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="0ab8a-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="0ab8a-129">**ID3DXRenderToSurface::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="0ab8a-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
