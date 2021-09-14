---
description: Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular objetos de malla.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interfaz ID3DX10Mesh (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddf0876928f85debded1645b9a22de790917017
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888825"
---
# <a name="id3dx10mesh-interface"></a>Interfaz ID3DX10Mesh

Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular objetos de malla.

## <a name="members"></a>Members

La **interfaz ID3DX10Mesh** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Mesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10Mesh** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Crea una nueva malla y la rellena con los datos de una malla cargada previamente.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Confirme los cambios realizados en una malla en el dispositivo para que se puedan representar. Se debe llamar a esto después de modificar los datos de una malla y antes de representarse. Una malla no se puede representar a menos que se haya confirmado en el dispositivo. Vea Notas.<br/>                                                                         |
| [**Discard (Descartar)**](id3dx10mesh-discard.md)                                                   | Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Dibuja un subconjunto de una malla.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Dibuje varias instancias del mismo subconjunto de una malla.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Genere un búfer de atributos a partir de los datos de la tabla de atributos de la malla. Un búfer de atributos es otro formato para almacenar los datos en la tabla de atributos. Tanto el búfer de atributos como la tabla de atributos son estructuras de datos internas en la malla.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Agrega datos de adyacencia al búfer de índice de la malla. Cuando la malla se va a enviar a un sombreador de geometría que toma datos de adyacencia, es necesario que el búfer de índice de la malla contenga datos de adyacencia.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Acceda al búfer de adyacencia de la malla.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Acceda al búfer de atributos de la malla.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Acceda al búfer de índice de la malla después de que se haya confirmado en el dispositivo [**con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Acceda al búfer de vértices de la malla después de que se haya confirmado en el dispositivo [**con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera el número de caras de la malla.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Acceda a las marcas de creación de la malla.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera los datos de un búfer de índice.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Obtenga el búfer de punto de réplica de la malla.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera el búfer de vértices asociado a la malla.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Obtiene el número de búferes de vértices de la malla.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Obtiene el número de vértices de la malla. Una malla puede contener varios búferes de vértice (es decir, un búfer de vértice puede contener todos los datos de posición, otro puede contener todos los datos de coordenadas de textura, etc.), pero cada búfer de vértice contendrá el mismo número de elementos.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Acceda a la descripción del vértice pasada a [**D3DX10CreateMesh.**](d3d10-d3dx10createmesh.md) La descripción del vértice describe el diseño de los búferes de vértice de la malla.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Determina si un rayo forma una intersección con esta malla.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina si un rayo forma una intersección con un subconjunto de esta malla.<br/>                                                                                                                                                                                                                                                                |
| [**Optimización**](id3dx10mesh-optimize.md)                                                 | Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Establezca los datos de adyacencia de la malla.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Establezca los datos de atributo de la malla.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Establezca los datos de índice de la malla.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Establezca los datos de la réplica de punto para la malla.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Establezca los datos de vértice en uno de los búferes de vértice de la malla.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Para obtener la interfaz ID3DX10Mesh, llame a [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
