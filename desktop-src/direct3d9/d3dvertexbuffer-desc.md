---
description: Describe un búfer de vértices.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: D3DVERTEXBUFFER_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548006"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="63515-103">D3DVERTEXBUFFER \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="63515-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="63515-104">Describe un búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="63515-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="63515-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63515-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="63515-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="63515-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="63515-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="63515-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="63515-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-109">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie de los datos del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="63515-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="63515-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="63515-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="63515-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-112">Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como un búfer de vértice.</span><span class="sxs-lookup"><span data-stu-id="63515-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="63515-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="63515-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="63515-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-115">Combinación de una o varias marcas de [**D3DUSAGE**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="63515-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="63515-116">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="63515-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="63515-117">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-118">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para este búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="63515-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="63515-119">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="63515-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="63515-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-121">Tamaño del búfer de vértices, en bytes.</span><span class="sxs-lookup"><span data-stu-id="63515-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="63515-122">**FVF**</span><span class="sxs-lookup"><span data-stu-id="63515-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="63515-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63515-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63515-124">Combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértice de los vértices de este búfer.</span><span class="sxs-lookup"><span data-stu-id="63515-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63515-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63515-125">Requirements</span></span>



| <span data-ttu-id="63515-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63515-126">Requirement</span></span> | <span data-ttu-id="63515-127">Value</span><span class="sxs-lookup"><span data-stu-id="63515-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63515-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63515-128">Header</span></span><br/> | <dl> <span data-ttu-id="63515-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="63515-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63515-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="63515-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63515-131">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="63515-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="63515-132">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="63515-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="63515-133">Búferes de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63515-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
