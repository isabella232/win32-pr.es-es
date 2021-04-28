---
description: 'D3DX10_ATTRIBUTE_RANGE estructura: almacena una entrada de tabla de atributos.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094373"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="8ca4b-103">Estructura D3DX10 \_ ATTRIBUTE \_ RANGE</span><span class="sxs-lookup"><span data-stu-id="8ca4b-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="8ca4b-104">Almacena una entrada de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ca4b-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="8ca4b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ca4b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ca4b-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="8ca4b-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ca4b-109">Identificador de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ca4b-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="8ca4b-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ca4b-112">Cara inicial.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="8ca4b-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="8ca4b-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ca4b-115">Recuento de caras.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="8ca4b-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="8ca4b-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ca4b-118">Vértice inicial.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="8ca4b-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="8ca4b-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ca4b-121">Recuento de vértices.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ca4b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ca4b-122">Remarks</span></span>

<span data-ttu-id="8ca4b-123">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="8ca4b-124">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="8ca4b-125">El tipo LPD3DX ATTRIBUTE RANGE se define como un \_ puntero a la estructura \_ D3DX \_ ATTRIBUTE \_ RANGE.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="8ca4b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca4b-126">Requirements</span></span>



| <span data-ttu-id="8ca4b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca4b-127">Requirement</span></span> | <span data-ttu-id="8ca4b-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ca4b-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca4b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca4b-129">Header</span></span><br/> | <dl> <span data-ttu-id="8ca4b-130"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4b-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca4b-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ca4b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca4b-132">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="8ca4b-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
