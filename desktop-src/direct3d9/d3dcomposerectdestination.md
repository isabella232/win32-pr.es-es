---
description: Especifica el glifo de origen y la ubicación en una superficie monocroma en la que copiar los glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estructura D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717664"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="4a670-103">Estructura D3DCOMPOSERECTDESTINATION</span><span class="sxs-lookup"><span data-stu-id="4a670-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="4a670-104">Especifica el glifo de origen y la ubicación en una superficie monocroma en la que copiar los glifos.</span><span class="sxs-lookup"><span data-stu-id="4a670-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a670-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a670-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="4a670-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a670-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a670-107">**SrcRectIndex**</span><span class="sxs-lookup"><span data-stu-id="4a670-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4a670-108">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a670-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a670-109">Glifo determinado del índice del búfer de vértices que contiene estructuras [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .</span><span class="sxs-lookup"><span data-stu-id="4a670-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="4a670-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="4a670-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="4a670-111">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a670-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a670-112">Reservado para la alineación.</span><span class="sxs-lookup"><span data-stu-id="4a670-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="4a670-113">**X**</span><span class="sxs-lookup"><span data-stu-id="4a670-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="4a670-114">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a670-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a670-115">Coordenada izquierda en la que se va a comenzar la copia.</span><span class="sxs-lookup"><span data-stu-id="4a670-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="4a670-116">**S**</span><span class="sxs-lookup"><span data-stu-id="4a670-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="4a670-117">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a670-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a670-118">Coordenada superior en la que se va a comenzar la copia.</span><span class="sxs-lookup"><span data-stu-id="4a670-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a670-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a670-119">Remarks</span></span>

<span data-ttu-id="4a670-120">Esta estructura se utiliza en las llamadas a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar que los glifos de ubicación se deben copiar en y qué glifo determinado debe copiarse.</span><span class="sxs-lookup"><span data-stu-id="4a670-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="4a670-121">Se crea un búfer de vértices (vea [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) rellenado con estas estructuras para que contenga las ubicaciones del glifo.</span><span class="sxs-lookup"><span data-stu-id="4a670-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="4a670-122">Los miembros USHORT se usan para reducir la superficie de memoria tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="4a670-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a670-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a670-123">Requirements</span></span>



| <span data-ttu-id="4a670-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a670-124">Requirement</span></span> | <span data-ttu-id="4a670-125">Value</span><span class="sxs-lookup"><span data-stu-id="4a670-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a670-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a670-126">Header</span></span><br/> | <dl> <span data-ttu-id="4a670-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a670-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a670-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a670-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a670-129">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4a670-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
