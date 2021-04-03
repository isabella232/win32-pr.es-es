---
description: Describe un subconjunto de la malla que tiene la misma combinación de atributo y hueso.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Estructura D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083743"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="2ab6a-103">Estructura D3DXBONECOMBINATION</span><span class="sxs-lookup"><span data-stu-id="2ab6a-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="2ab6a-104">Describe un subconjunto de la malla que tiene la misma combinación de atributo y hueso.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ab6a-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="2ab6a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ab6a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ab6a-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-109">Identificador de la tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2ab6a-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-112">Superficie inicial.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="2ab6a-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-115">Recuento de caras.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="2ab6a-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-118">Vértice inicial.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="2ab6a-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-121">Recuento de vértices.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="2ab6a-122">**BoneId**</span><span class="sxs-lookup"><span data-stu-id="2ab6a-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="2ab6a-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ab6a-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="2ab6a-124">Puntero a una matriz de valores que identifican cada uno de los huesos que se pueden dibujar en una sola llamada de dibujo.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="2ab6a-125">Tenga en cuenta que la matriz puede ser de longitud variable para dar cabida a las combinaciones de longitud variable de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span><span class="sxs-lookup"><span data-stu-id="2ab6a-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="2ab6a-126">El tamaño de la matriz varía en función del tipo de malla generado.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="2ab6a-127">Un tamaño de matriz de malla sin indexar es igual al número de pesos por vértice (pMaxVertexInfl en [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="2ab6a-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="2ab6a-128">Un tamaño de matriz de malla indizada es igual al número de entradas de la paleta de la matriz de huesos (paletteSize en [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="2ab6a-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ab6a-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ab6a-129">Remarks</span></span>

<span data-ttu-id="2ab6a-130">El subconjunto de la malla descrito por **D3DXBONECOMBINATION** se puede representar en una sola llamada de dibujo.</span><span class="sxs-lookup"><span data-stu-id="2ab6a-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab6a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ab6a-131">Requirements</span></span>



| <span data-ttu-id="2ab6a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab6a-132">Requirement</span></span> | <span data-ttu-id="2ab6a-133">Value</span><span class="sxs-lookup"><span data-stu-id="2ab6a-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab6a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ab6a-134">Header</span></span><br/> | <dl> <span data-ttu-id="2ab6a-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ab6a-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab6a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ab6a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab6a-137">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="2ab6a-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
