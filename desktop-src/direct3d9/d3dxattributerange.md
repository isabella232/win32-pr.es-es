---
description: 'Estructura D3DXATTRIBUTERANGE: almacena una entrada de tabla de atributos.'
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Estructura D3DXATTRIBUTERANGE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116022"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="aa4d9-103">D3DXATTRIBUTERANGE (estructura)</span><span class="sxs-lookup"><span data-stu-id="aa4d9-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="aa4d9-104">Almacena una entrada de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa4d9-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="aa4d9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa4d9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa4d9-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="aa4d9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aa4d9-109">Identificador de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="aa4d9-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="aa4d9-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aa4d9-112">Cara inicial.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="aa4d9-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="aa4d9-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aa4d9-115">Recuento de caras.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="aa4d9-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="aa4d9-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aa4d9-118">Vértice inicial.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="aa4d9-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="aa4d9-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aa4d9-121">Recuento de vértices.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa4d9-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa4d9-122">Remarks</span></span>

<span data-ttu-id="aa4d9-123">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="aa4d9-124">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="aa4d9-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="aa4d9-125">El tipo LPD3DXATTRIBUTERANGE se define como un puntero a la **estructura D3DXATTRIBUTERANGE.**</span><span class="sxs-lookup"><span data-stu-id="aa4d9-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="aa4d9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4d9-126">Requirements</span></span>



| <span data-ttu-id="aa4d9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4d9-127">Requirement</span></span> | <span data-ttu-id="aa4d9-128">Value</span><span class="sxs-lookup"><span data-stu-id="aa4d9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4d9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa4d9-129">Header</span></span><br/> | <dl> <span data-ttu-id="aa4d9-130"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4d9-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4d9-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa4d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4d9-132">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="aa4d9-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
