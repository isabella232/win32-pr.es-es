---
description: Opciones de soldadura entre vértices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumeración D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362607"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="117c1-103">Enumeración D3DXWELDEPSILONSFLAGS</span><span class="sxs-lookup"><span data-stu-id="117c1-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="117c1-104">Opciones de soldadura entre vértices.</span><span class="sxs-lookup"><span data-stu-id="117c1-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="117c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="117c1-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="117c1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="117c1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="117c1-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**</span><span class="sxs-lookup"><span data-stu-id="117c1-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="117c1-108">Soldadura juntas todos los vértices que se encuentran en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="117c1-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="117c1-109">El uso de esta marca evita una comparación de épsilon entre los componentes de vértices.</span><span class="sxs-lookup"><span data-stu-id="117c1-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="117c1-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**</span><span class="sxs-lookup"><span data-stu-id="117c1-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="117c1-111">Si un componente de vértice determinado está en épsilon, modifique los vértices parcialmente coincidentes para que ambos componentes sean idénticos.</span><span class="sxs-lookup"><span data-stu-id="117c1-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="117c1-112">Si todos los componentes son iguales, Quite uno de los vértices.</span><span class="sxs-lookup"><span data-stu-id="117c1-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="117c1-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**</span><span class="sxs-lookup"><span data-stu-id="117c1-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="117c1-114">Indica a la soldadura que solo permita modificaciones en los vértices y no en la eliminación.</span><span class="sxs-lookup"><span data-stu-id="117c1-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="117c1-115">Esta marca solo es válida si \_ se establece D3DXWELDEPSILONS WELDPARTIALMATCHES.</span><span class="sxs-lookup"><span data-stu-id="117c1-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="117c1-116">Resulta útil modificar los vértices para que sean iguales, pero no para permitir que se quiten los vértices.</span><span class="sxs-lookup"><span data-stu-id="117c1-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="117c1-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="117c1-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="117c1-118">Indica a la soldadura que no divida los vértices que se encuentran en grupos de atributos independientes.</span><span class="sxs-lookup"><span data-stu-id="117c1-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="117c1-119">Cuando se llama al método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con la \_ marca ATTRSORT de D3DXMESHOPT, \_ también se establecerá la marca D3DXMESHOPT DONOTSPLIT.</span><span class="sxs-lookup"><span data-stu-id="117c1-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="117c1-120">La configuración de esta marca puede ralentizar el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="117c1-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="117c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="117c1-121">Requirements</span></span>



| <span data-ttu-id="117c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="117c1-122">Requirement</span></span> | <span data-ttu-id="117c1-123">Value</span><span class="sxs-lookup"><span data-stu-id="117c1-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="117c1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="117c1-124">Header</span></span><br/> | <dl> <span data-ttu-id="117c1-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="117c1-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="117c1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="117c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="117c1-127">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="117c1-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="117c1-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="117c1-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 




