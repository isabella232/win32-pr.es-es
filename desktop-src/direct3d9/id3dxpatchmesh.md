---
description: Esta interfaz encapsula la funcionalidad de malla de revisión.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interfaz ID3DXPatchMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 44899ccee6f13aa25b01e284df5a892196d657610c3f89d546fc0b646eeaa069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856285"
---
# <a name="id3dxpatchmesh-interface"></a>Interfaz ID3DXPatchMesh

Esta interfaz encapsula la funcionalidad de malla de revisión.

## <a name="members"></a>Miembros

La **interfaz ID3DXPatchMesh** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPatchMesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXPatchMesh** tiene estos métodos.



| Método                                                                           | Descripción                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Crea una nueva malla de revisión con la declaración de vértice especificada.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Genere una lista de bordes de malla y las revisiones que comparten cada borde.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Obtiene el número de vértices de control por revisión.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Obtiene la declaración de vértice.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Obtiene el dispositivo que creó la malla.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Obtiene los parámetros de desplazamiento de geometría de malla.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Obtiene el búfer de índice de malla.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Obtiene el número de revisiones de la malla.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Obtiene el número de vértices de la malla.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Obtiene el tipo de revisión.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Obtiene los atributos de la revisión.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Obtiene el tamaño de la malla teselada, dado un nivel de teselación.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Obtiene el búfer de vértices de malla.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Bloquea el búfer de atributos.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Bloquee el búfer de índice.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Bloquee el búfer de vértices.<br/>                                                              |
| [**Optimización**](id3dxpatchmesh--optimize.md)                                     | Optimiza la malla de revisión para una teselación eficaz.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Establece parámetros de desplazamiento de geometría de malla.<br/>                                          |
| [**Tessellate**](id3dxpatchmesh--tessellate.md)                                 | Realiza una teselación uniforme en función del nivel de teselación.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Realiza la teselación adaptable en función del criterio de teselación adaptable basado en z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Desbloquee el búfer de atributos.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Desbloquee el búfer de índice.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Desbloquee el búfer de vértices.<br/>                                                            |



 

## <a name="remarks"></a>Comentarios

Una malla de revisión es una malla que consta de una serie de revisiones.

Para obtener la **interfaz ID3DXPatchMesh,** llame a la función [**D3DXCreatePatchMesh.**](d3dxcreatepatchmesh.md)

El tipo LPD3DXPATCHMESH se define como un puntero a la interfaz **ID3DXPatchMesh,** como se indica a continuación:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
