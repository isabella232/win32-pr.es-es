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
# <a name="id3dxpatchmesh-interface"></a>Interfaz ID3DXPatchMesh

Esta interfaz encapsula la funcionalidad de la malla de revisiones.

## <a name="members"></a>Miembros

La interfaz **ID3DXPatchMesh** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPatchMesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXPatchMesh** tiene estos métodos.



| Método                                                                           | Descripción                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Crea una nueva malla de revisión con la declaración de vértice especificada.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Generar una lista de bordes de malla y las revisiones que comparten cada borde.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Obtiene el número de vértices de control por revisión.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Obtiene la declaración de vértice.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Obtiene el dispositivo que creó la malla.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Obtiene los parámetros de desplazamiento de geometría de la malla.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Obtiene el búfer de índice de malla.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Obtiene el número de revisiones en la malla.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Obtiene el número de vértices de la malla.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Obtiene el tipo de revisión.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Obtiene los atributos de la revisión.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Obtiene el tamaño de la malla teselada, dado un nivel de teselación.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Obtiene el búfer de vértices de malla.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Bloquea el búfer de atributo.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Bloquee el búfer de índice.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Bloquee el búfer de vértices.<br/>                                                              |
| [**Optimización**](id3dxpatchmesh--optimize.md)                                     | Optimiza la malla de revisión para una teselación eficaz.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Establece los parámetros de desplazamiento de la geometría de malla.<br/>                                          |
| [**Dividirlas**](id3dxpatchmesh--tessellate.md)                                 | Realiza una teselación uniforme basada en el nivel de teselación.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Realiza una teselación adaptativa basada en el criterio de teselación adaptable basado en z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Desbloquee el búfer de atributo.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Desbloquee el búfer de índice.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Desbloquee el búfer de vértices.<br/>                                                            |



 

## <a name="remarks"></a>Observaciones

Una malla de revisión es una malla que consta de una serie de revisiones.

Para obtener la interfaz **ID3DXPatchMesh** , llame a la función [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .

El tipo LPD3DXPATCHMESH se define como un puntero a la interfaz **ID3DXPatchMesh** , como se indica a continuación:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
