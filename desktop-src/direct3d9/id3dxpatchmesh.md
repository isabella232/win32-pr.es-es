---
description: Esta interfaz encapsula la funcionalidad de la malla de revisiones.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interfaz ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362641"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="47e0d-103">Interfaz ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="47e0d-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="47e0d-104">Esta interfaz encapsula la funcionalidad de la malla de revisiones.</span><span class="sxs-lookup"><span data-stu-id="47e0d-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="47e0d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="47e0d-105">Members</span></span>

<span data-ttu-id="47e0d-106">La interfaz **ID3DXPatchMesh** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="47e0d-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47e0d-107">**ID3DXPatchMesh** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47e0d-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="47e0d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="47e0d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47e0d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="47e0d-109">Methods</span></span>

<span data-ttu-id="47e0d-110">La interfaz **ID3DXPatchMesh** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="47e0d-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="47e0d-111">Método</span><span class="sxs-lookup"><span data-stu-id="47e0d-111">Method</span></span>                                                                           | <span data-ttu-id="47e0d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="47e0d-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47e0d-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="47e0d-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="47e0d-114">Crea una nueva malla de revisión con la declaración de vértice especificada.</span><span class="sxs-lookup"><span data-stu-id="47e0d-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="47e0d-115">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="47e0d-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="47e0d-116">Generar una lista de bordes de malla y las revisiones que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="47e0d-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="47e0d-117">**GetControlVerticesPerPatch**</span><span class="sxs-lookup"><span data-stu-id="47e0d-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="47e0d-118">Obtiene el número de vértices de control por revisión.</span><span class="sxs-lookup"><span data-stu-id="47e0d-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="47e0d-119">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="47e0d-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="47e0d-120">Obtiene la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="47e0d-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="47e0d-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="47e0d-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="47e0d-122">Obtiene el dispositivo que creó la malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="47e0d-123">**GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="47e0d-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="47e0d-124">Obtiene los parámetros de desplazamiento de geometría de la malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="47e0d-125">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="47e0d-126">Obtiene el búfer de índice de malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="47e0d-127">**GetNumPatches**</span><span class="sxs-lookup"><span data-stu-id="47e0d-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="47e0d-128">Obtiene el número de revisiones en la malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="47e0d-129">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="47e0d-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="47e0d-130">Obtiene el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="47e0d-131">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="47e0d-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="47e0d-132">Obtiene el tipo de revisión.</span><span class="sxs-lookup"><span data-stu-id="47e0d-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="47e0d-133">**GetPatchInfo**</span><span class="sxs-lookup"><span data-stu-id="47e0d-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="47e0d-134">Obtiene los atributos de la revisión.</span><span class="sxs-lookup"><span data-stu-id="47e0d-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="47e0d-135">**GetTessSize**</span><span class="sxs-lookup"><span data-stu-id="47e0d-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="47e0d-136">Obtiene el tamaño de la malla teselada, dado un nivel de teselación.</span><span class="sxs-lookup"><span data-stu-id="47e0d-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="47e0d-137">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="47e0d-138">Obtiene el búfer de vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="47e0d-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="47e0d-140">Bloquea el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="47e0d-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="47e0d-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="47e0d-142">Bloquee el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="47e0d-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="47e0d-143">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="47e0d-144">Bloquee el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="47e0d-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="47e0d-145">**Optimización**</span><span class="sxs-lookup"><span data-stu-id="47e0d-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="47e0d-146">Optimiza la malla de revisión para una teselación eficaz.</span><span class="sxs-lookup"><span data-stu-id="47e0d-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="47e0d-147">**SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="47e0d-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="47e0d-148">Establece los parámetros de desplazamiento de la geometría de malla.</span><span class="sxs-lookup"><span data-stu-id="47e0d-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="47e0d-149">**Dividirlas**</span><span class="sxs-lookup"><span data-stu-id="47e0d-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="47e0d-150">Realiza una teselación uniforme basada en el nivel de teselación.</span><span class="sxs-lookup"><span data-stu-id="47e0d-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="47e0d-151">**TessellateAdaptive**</span><span class="sxs-lookup"><span data-stu-id="47e0d-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="47e0d-152">Realiza una teselación adaptativa basada en el criterio de teselación adaptable basado en z.</span><span class="sxs-lookup"><span data-stu-id="47e0d-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="47e0d-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="47e0d-154">Desbloquee el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="47e0d-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="47e0d-155">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="47e0d-156">Desbloquee el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="47e0d-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="47e0d-157">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e0d-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="47e0d-158">Desbloquee el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="47e0d-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="47e0d-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47e0d-159">Remarks</span></span>

<span data-ttu-id="47e0d-160">Una malla de revisión es una malla que consta de una serie de revisiones.</span><span class="sxs-lookup"><span data-stu-id="47e0d-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="47e0d-161">Para obtener la interfaz **ID3DXPatchMesh** , llame a la función [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="47e0d-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="47e0d-162">El tipo LPD3DXPATCHMESH se define como un puntero a la interfaz **ID3DXPatchMesh** , como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="47e0d-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="47e0d-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e0d-163">Requirements</span></span>



| <span data-ttu-id="47e0d-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e0d-164">Requirement</span></span> | <span data-ttu-id="47e0d-165">Value</span><span class="sxs-lookup"><span data-stu-id="47e0d-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47e0d-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47e0d-166">Header</span></span><br/>  | <dl> <span data-ttu-id="47e0d-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e0d-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="47e0d-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47e0d-168">Library</span></span><br/> | <dl> <span data-ttu-id="47e0d-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47e0d-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47e0d-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="47e0d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e0d-171">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="47e0d-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="47e0d-172">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="47e0d-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
