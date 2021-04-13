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
# <a name="id3dxbasemesh-interface"></a>Interfaz ID3DXBaseMesh

Las aplicaciones usan los métodos de la interfaz **ID3DXBaseMesh** para manipular y consultar objetos de malla progresiva y de malla.

## <a name="members"></a>Miembros

La interfaz **ID3DXBaseMesh** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseMesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXBaseMesh** tiene estos métodos.



| Método                                                                            | Descripción                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxbasemesh--clonemesh.md)                                     | Clona una malla mediante un declarador.<br/>                                                                                                                                                                          |
| [**CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)                               | Clona una malla con un código de formato de vértice flexible (FVF).<br/>                                                                                                                                                   |
| [**ConvertAdjacencyToPointReps**](id3dxbasemesh--convertadjacencytopointreps.md) | Convierte la información de proximidad de la malla en una matriz de representantes de puntos.<br/>                                                                                                                                  |
| [**ConvertPointRepsToAdjacency**](id3dxbasemesh--convertpointrepstoadjacency.md) | Convierte los datos representativos de punto en información de adyacencia de malla.<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | Dibuja un subconjunto de una malla.<br/>                                                                                                                                                                                  |
| [**GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)                     | Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.<br/>                                                                                                                            |
| [**GetAttributeTable**](id3dxbasemesh--getattributetable.md)                     | Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.<br/>                                                                                          |
| [**GetDeclaration**](id3dxbasemesh--getdeclaration.md)                           | Recupera una declaración que describe los vértices de la malla.<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | Recupera el dispositivo asociado a la malla.<br/>                                                                                                                                                             |
| [**GetFVF**](id3dxbasemesh--getfvf.md)                                           | Obtiene el valor de vértice de función fijo.<br/>                                                                                                                                                                      |
| [**GetIndexBuffer**](id3dxbasemesh--getindexbuffer.md)                           | Recupera los datos en un búfer de índice.<br/>                                                                                                                                                                     |
| [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)               | Obtiene el número de bytes por vértice.<br/>                                                                                                                                                                       |
| [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)                                 | Recupera el número de caras de la malla.<br/>                                                                                                                                                                 |
| [**GetNumVertices**](id3dxbasemesh--getnumvertices.md)                           | Recupera el número de vértices de la malla.<br/>                                                                                                                                                              |
| [**GetOptions**](id3dxbasemesh--getoptions.md)                                   | Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.<br/>                                                                                                                                         |
| [**GetVertexBuffer**](id3dxbasemesh--getvertexbuffer.md)                         | Recupera el búfer de vértices asociado a la malla.<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | Bloquea un búfer de índice y obtiene un puntero a la memoria del búfer de índice.<br/>                                                                                                                                    |
| [**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.<br/>                                                                                                                                   |
| [**UnlockIndexBuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | Desbloquea un búfer de índice.<br/>                                                                                                                                                                                   |
| [**UnlockVertexBuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | Desbloquea un búfer de vértices.<br/>                                                                                                                                                                                   |
| [**UpdateSemantics**](id3dxbasemesh--updatesemantics.md)                         | Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices. La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.<br/> |



 

## <a name="remarks"></a>Observaciones

Una malla es un objeto compuesto por un conjunto de caras poligonales. Una malla define un conjunto de vértices y un conjunto de caras (las caras se definen en términos de vértices y normales de la malla).

El tipo LPD3DXBASEMESH se define como un puntero a la interfaz **ID3DXBaseMesh** .


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
