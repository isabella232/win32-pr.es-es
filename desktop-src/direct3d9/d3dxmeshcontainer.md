---
description: Encapsula un objeto Mesh en una jerarquía de fotogramas de transformación.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Estructura D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362435"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="302a4-103">Estructura D3DXMESHCONTAINER</span><span class="sxs-lookup"><span data-stu-id="302a4-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="302a4-104">Encapsula un objeto Mesh en una jerarquía de fotogramas de transformación.</span><span class="sxs-lookup"><span data-stu-id="302a4-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="302a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="302a4-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="302a4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="302a4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="302a4-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="302a4-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="302a4-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-109">Nombre de la malla.</span><span class="sxs-lookup"><span data-stu-id="302a4-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="302a4-110">**MeshData**</span><span class="sxs-lookup"><span data-stu-id="302a4-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-111">Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="302a4-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-112">Tipo de datos en la malla.</span><span class="sxs-lookup"><span data-stu-id="302a4-112">Type of data in the mesh.</span></span> <span data-ttu-id="302a4-113">Vea [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="302a4-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="302a4-114">**pMaterials**</span><span class="sxs-lookup"><span data-stu-id="302a4-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-115">Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="302a4-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-116">Matriz de materiales de malla.</span><span class="sxs-lookup"><span data-stu-id="302a4-116">Array of mesh materials.</span></span> <span data-ttu-id="302a4-117">Vea [**D3DXMATERIAL**](d3dxmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="302a4-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="302a4-118">**pEffects**</span><span class="sxs-lookup"><span data-stu-id="302a4-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-119">Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="302a4-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-120">Puntero a un conjunto de parámetros de efectos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="302a4-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="302a4-121">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="302a4-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="302a4-122">**NumMaterials**</span><span class="sxs-lookup"><span data-stu-id="302a4-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302a4-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-124">Número de materiales en la malla.</span><span class="sxs-lookup"><span data-stu-id="302a4-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="302a4-125">**pAdjacency**</span><span class="sxs-lookup"><span data-stu-id="302a4-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302a4-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="302a4-127">Puntero a una matriz de tres DWORDs por triángulo de la malla que contiene información de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="302a4-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="302a4-128">**pSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="302a4-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-129">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="302a4-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="302a4-130">Puntero a la interfaz de información de máscara.</span><span class="sxs-lookup"><span data-stu-id="302a4-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="302a4-131">Vea [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="302a4-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="302a4-132">**pNextMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="302a4-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="302a4-133">Tipo: \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="302a4-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="302a4-134">Puntero al siguiente contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="302a4-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="302a4-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="302a4-135">Remarks</span></span>

<span data-ttu-id="302a4-136">Una aplicación puede derivar de esta estructura para agregar otros datos.</span><span class="sxs-lookup"><span data-stu-id="302a4-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="302a4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="302a4-137">Requirements</span></span>



| <span data-ttu-id="302a4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="302a4-138">Requirement</span></span> | <span data-ttu-id="302a4-139">Value</span><span class="sxs-lookup"><span data-stu-id="302a4-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="302a4-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="302a4-140">Header</span></span><br/> | <dl> <span data-ttu-id="302a4-141"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="302a4-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="302a4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="302a4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302a4-143">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="302a4-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
