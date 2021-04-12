---
description: Las aplicaciones usan los métodos de la interfaz ID3DXMesh para manipular los objetos de malla.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interfaz ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362742"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="fa657-103">Interfaz ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="fa657-103">ID3DXMesh interface</span></span>

<span data-ttu-id="fa657-104">Las aplicaciones usan los métodos de la interfaz ID3DXMesh para manipular los objetos de malla.</span><span class="sxs-lookup"><span data-stu-id="fa657-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="fa657-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa657-105">Members</span></span>

<span data-ttu-id="fa657-106">La interfaz **ID3DXMesh** hereda de [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="fa657-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="fa657-107">**ID3DXMesh** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fa657-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="fa657-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa657-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa657-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa657-109">Methods</span></span>

<span data-ttu-id="fa657-110">La interfaz **ID3DXMesh** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fa657-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="fa657-111">Método</span><span class="sxs-lookup"><span data-stu-id="fa657-111">Method</span></span>                                                            | <span data-ttu-id="fa657-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa657-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa657-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="fa657-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="fa657-114">Bloquea el búfer de malla que contiene los datos de atributo de la malla y devuelve un puntero a él.</span><span class="sxs-lookup"><span data-stu-id="fa657-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="fa657-115">**Optimización**</span><span class="sxs-lookup"><span data-stu-id="fa657-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="fa657-116">Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="fa657-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="fa657-117">**OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="fa657-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="fa657-118">Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="fa657-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="fa657-119">Este método reordena la malla existente.</span><span class="sxs-lookup"><span data-stu-id="fa657-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="fa657-120">**SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="fa657-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="fa657-121">Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="fa657-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="fa657-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="fa657-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="fa657-123">Desbloquea un búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="fa657-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="fa657-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa657-124">Remarks</span></span>

<span data-ttu-id="fa657-125">Para obtener la interfaz **ID3DXMesh** , llame a la función [**D3DXCreateMesh**](d3dxcreatemesh.md) o [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="fa657-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="fa657-126">Esta interfaz hereda funcionalidad adicional de la interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) .</span><span class="sxs-lookup"><span data-stu-id="fa657-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="fa657-127">El tipo LPD3DXMESH se define como un puntero a la interfaz **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="fa657-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="fa657-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa657-128">Requirements</span></span>



| <span data-ttu-id="fa657-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa657-129">Requirement</span></span> | <span data-ttu-id="fa657-130">Value</span><span class="sxs-lookup"><span data-stu-id="fa657-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa657-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa657-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fa657-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa657-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fa657-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa657-133">Library</span></span><br/> | <dl> <span data-ttu-id="fa657-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa657-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa657-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa657-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa657-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="fa657-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="fa657-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="fa657-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fa657-138">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="fa657-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




