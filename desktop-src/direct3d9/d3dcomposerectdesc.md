---
description: Especifica el rectángulo que se usa para incluir glifos en una superficie monocroma.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Estructura D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424347"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="6518f-103">Estructura D3DCOMPOSERECTDESC</span><span class="sxs-lookup"><span data-stu-id="6518f-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="6518f-104">Especifica el rectángulo que se usa para incluir glifos en una superficie monocroma.</span><span class="sxs-lookup"><span data-stu-id="6518f-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6518f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6518f-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="6518f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6518f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6518f-107">**X**</span><span class="sxs-lookup"><span data-stu-id="6518f-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="6518f-108">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6518f-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6518f-109">Coordenada izquierda en la que se va a comenzar la copia.</span><span class="sxs-lookup"><span data-stu-id="6518f-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="6518f-110">**S**</span><span class="sxs-lookup"><span data-stu-id="6518f-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="6518f-111">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6518f-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6518f-112">Coordenada superior en la que se va a comenzar la copia.</span><span class="sxs-lookup"><span data-stu-id="6518f-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="6518f-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="6518f-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="6518f-114">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6518f-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6518f-115">Número de textura de la coordenada izquierda.</span><span class="sxs-lookup"><span data-stu-id="6518f-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6518f-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="6518f-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="6518f-117">Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6518f-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6518f-118">Número de textura de la coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="6518f-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6518f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6518f-119">Remarks</span></span>

<span data-ttu-id="6518f-120">Esta estructura se utiliza en las llamadas a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir los glifos en la superficie de origen.</span><span class="sxs-lookup"><span data-stu-id="6518f-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="6518f-121">Se crea un búfer de vértices (vea [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) rellenado con estas estructuras para que contenga las ubicaciones del glifo.</span><span class="sxs-lookup"><span data-stu-id="6518f-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="6518f-122">Los miembros USHORT se usan para reducir la superficie de memoria tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="6518f-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="6518f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6518f-123">Requirements</span></span>



| <span data-ttu-id="6518f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6518f-124">Requirement</span></span> | <span data-ttu-id="6518f-125">Value</span><span class="sxs-lookup"><span data-stu-id="6518f-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6518f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6518f-126">Header</span></span><br/> | <dl> <span data-ttu-id="6518f-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6518f-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6518f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6518f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6518f-129">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6518f-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
