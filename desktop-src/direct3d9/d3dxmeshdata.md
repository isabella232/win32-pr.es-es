---
description: Estructura de datos de malla.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: Estructura D3DXMESHDATA (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362434"
---
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="35461-103">Estructura D3DXMESHDATA</span><span class="sxs-lookup"><span data-stu-id="35461-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="35461-104">Estructura de datos de malla.</span><span class="sxs-lookup"><span data-stu-id="35461-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="35461-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35461-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="35461-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="35461-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="35461-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="35461-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="35461-108">Tipo: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="35461-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35461-109">Define el tipo de datos de la malla.</span><span class="sxs-lookup"><span data-stu-id="35461-109">Defines the mesh data type.</span></span> <span data-ttu-id="35461-110">Vea [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span><span class="sxs-lookup"><span data-stu-id="35461-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="35461-111">**pMesh**</span><span class="sxs-lookup"><span data-stu-id="35461-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="35461-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="35461-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="35461-113">Puntero a una malla.</span><span class="sxs-lookup"><span data-stu-id="35461-113">Pointer to a mesh.</span></span> <span data-ttu-id="35461-114">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="35461-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="35461-115">**pPatchMesh**</span><span class="sxs-lookup"><span data-stu-id="35461-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="35461-116">Tipo: **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="35461-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="35461-117">Puntero a una malla de revisión.</span><span class="sxs-lookup"><span data-stu-id="35461-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="35461-118">Vea [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="35461-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35461-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35461-119">Requirements</span></span>



| <span data-ttu-id="35461-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35461-120">Requirement</span></span> | <span data-ttu-id="35461-121">Value</span><span class="sxs-lookup"><span data-stu-id="35461-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35461-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35461-122">Header</span></span><br/> | <dl> <span data-ttu-id="35461-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="35461-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35461-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="35461-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35461-125">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="35461-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="35461-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="35461-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 
