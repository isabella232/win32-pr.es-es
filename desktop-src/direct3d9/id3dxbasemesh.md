---
description: Las aplicaciones usan los métodos de la interfaz ID3DXBaseMesh para manipular y consultar objetos de malla progresiva y de malla.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interfaz ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362605"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="ad9c2-103">Interfaz ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="ad9c2-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="ad9c2-104">Las aplicaciones usan los métodos de la interfaz **ID3DXBaseMesh** para manipular y consultar objetos de malla progresiva y de malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="ad9c2-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad9c2-105">Members</span></span>

<span data-ttu-id="ad9c2-106">La interfaz **ID3DXBaseMesh** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ad9c2-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ad9c2-107">**ID3DXBaseMesh** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ad9c2-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="ad9c2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad9c2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad9c2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad9c2-109">Methods</span></span>

<span data-ttu-id="ad9c2-110">La interfaz **ID3DXBaseMesh** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="ad9c2-111">Método</span><span class="sxs-lookup"><span data-stu-id="ad9c2-111">Method</span></span>                                                                            | <span data-ttu-id="ad9c2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad9c2-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad9c2-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="ad9c2-114">Clona una malla mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="ad9c2-115">**CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="ad9c2-116">Clona una malla con un código de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="ad9c2-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="ad9c2-117">**ConvertAdjacencyToPointReps**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="ad9c2-118">Convierte la información de proximidad de la malla en una matriz de representantes de puntos.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ad9c2-119">**ConvertPointRepsToAdjacency**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="ad9c2-120">Convierte los datos representativos de punto en información de adyacencia de malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="ad9c2-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="ad9c2-122">Dibuja un subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="ad9c2-123">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="ad9c2-124">Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="ad9c2-125">**GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="ad9c2-126">Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="ad9c2-127">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="ad9c2-128">Recupera una declaración que describe los vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="ad9c2-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="ad9c2-130">Recupera el dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="ad9c2-131">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="ad9c2-132">Obtiene el valor de vértice de función fijo.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="ad9c2-133">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="ad9c2-134">Recupera los datos en un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="ad9c2-135">**GetNumBytesPerVertex**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="ad9c2-136">Obtiene el número de bytes por vértice.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="ad9c2-137">**GetNumFaces**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="ad9c2-138">Recupera el número de caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="ad9c2-139">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="ad9c2-140">Recupera el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="ad9c2-141">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="ad9c2-142">Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="ad9c2-143">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="ad9c2-144">Recupera el búfer de vértices asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="ad9c2-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="ad9c2-146">Bloquea un búfer de índice y obtiene un puntero a la memoria del búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="ad9c2-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="ad9c2-148">Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ad9c2-149">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="ad9c2-150">Desbloquea un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="ad9c2-151">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="ad9c2-152">Desbloquea un búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="ad9c2-153">**UpdateSemantics**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="ad9c2-154">Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="ad9c2-155">La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad9c2-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad9c2-156">Remarks</span></span>

<span data-ttu-id="ad9c2-157">Una malla es un objeto compuesto por un conjunto de caras poligonales.</span><span class="sxs-lookup"><span data-stu-id="ad9c2-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="ad9c2-158">Una malla define un conjunto de vértices y un conjunto de caras (las caras se definen en términos de vértices y normales de la malla).</span><span class="sxs-lookup"><span data-stu-id="ad9c2-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="ad9c2-159">El tipo LPD3DXBASEMESH se define como un puntero a la interfaz **ID3DXBaseMesh** .</span><span class="sxs-lookup"><span data-stu-id="ad9c2-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="ad9c2-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9c2-160">Requirements</span></span>



| <span data-ttu-id="ad9c2-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9c2-161">Requirement</span></span> | <span data-ttu-id="ad9c2-162">Value</span><span class="sxs-lookup"><span data-stu-id="ad9c2-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9c2-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad9c2-163">Header</span></span><br/>  | <dl> <span data-ttu-id="ad9c2-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c2-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad9c2-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad9c2-165">Library</span></span><br/> | <dl> <span data-ttu-id="ad9c2-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c2-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad9c2-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad9c2-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9c2-168">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="ad9c2-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
