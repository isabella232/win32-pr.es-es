---
description: Almacena una entrada de tabla de atributos.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Estructura D3DXATTRIBUTERANGE (D3dx9mesh. h)
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
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707919"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="4b875-103">Estructura D3DXATTRIBUTERANGE</span><span class="sxs-lookup"><span data-stu-id="4b875-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="4b875-104">Almacena una entrada de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="4b875-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b875-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b875-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="4b875-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b875-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b875-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="4b875-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="4b875-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b875-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b875-109">Identificador de la tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="4b875-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4b875-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="4b875-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="4b875-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b875-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b875-112">Superficie inicial.</span><span class="sxs-lookup"><span data-stu-id="4b875-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="4b875-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="4b875-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="4b875-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b875-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b875-115">Recuento de caras.</span><span class="sxs-lookup"><span data-stu-id="4b875-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="4b875-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="4b875-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="4b875-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b875-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b875-118">Vértice inicial.</span><span class="sxs-lookup"><span data-stu-id="4b875-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="4b875-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="4b875-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="4b875-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b875-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b875-121">Recuento de vértices.</span><span class="sxs-lookup"><span data-stu-id="4b875-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b875-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b875-122">Remarks</span></span>

<span data-ttu-id="4b875-123">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc.</span><span class="sxs-lookup"><span data-stu-id="4b875-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="4b875-124">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (AttribId) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="4b875-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="4b875-125">El tipo LPD3DXATTRIBUTERANGE se define como un puntero a la estructura **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="4b875-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="4b875-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b875-126">Requirements</span></span>



| <span data-ttu-id="4b875-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b875-127">Requirement</span></span> | <span data-ttu-id="4b875-128">Value</span><span class="sxs-lookup"><span data-stu-id="4b875-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b875-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b875-129">Header</span></span><br/> | <dl> <span data-ttu-id="4b875-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b875-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b875-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b875-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b875-132">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="4b875-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
