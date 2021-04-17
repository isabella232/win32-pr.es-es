---
description: Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular los objetos de malla.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interfaz ID3DX10Mesh (D3DX10. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698426"
---
# <a name="id3dx10mesh-interface"></a>Interfaz ID3DX10Mesh

Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular los objetos de malla.

## <a name="members"></a>Miembros

La interfaz **ID3DX10Mesh** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Mesh** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10Mesh** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Crea una nueva malla y la rellena con los datos de una malla cargada previamente.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Confirme los cambios realizados en una malla en el dispositivo para que los cambios se puedan representar. Se debe llamar a este método después de que se modifiquen los datos de una malla y antes de que se representen. No se puede representar una malla a menos que se confirme en el dispositivo. Vea Notas.<br/>                                                                         |
| [**Discard (Descartar)**](id3dx10mesh-discard.md)                                                   | Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Dibuja un subconjunto de una malla.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Dibuja varias instancias del mismo subconjunto de una malla.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Genere un búfer de atributo a partir de los datos de la tabla de atributos de la malla. Un búfer de atributo es otro formato para almacenar los datos en la tabla de atributos. Tanto el búfer de atributo como la tabla de atributos son estructuras de datos internas en la malla.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Agrega datos de adyacencia al búfer de índice de la malla. Cuando la malla se va a enviar a un sombreador de geometría que toma datos de adyacencias, es necesario que el búfer de índice de la malla contenga datos de adyacencia.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Obtenga acceso al búfer de adyacencia de la malla.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Obtenga acceso al búfer de atributo de la malla.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Obtenga acceso al búfer de índice de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Obtenga acceso al búfer de vértices de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera el número de caras de la malla.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Acceder a las marcas de creación de la malla.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera los datos en un búfer de índice.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Obtiene el búfer del representante de puntos de la malla.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera el búfer de vértices asociado a la malla.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Obtiene el número de búferes de vértices en la malla.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Obtiene el número de vértices en la malla. Una malla puede contener varios búferes de vértices (es decir, un búfer de vértices puede contener todos los datos de posición, otro puede contener todos los datos de coordenadas de textura, etc.); sin embargo, cada búfer de vértice contendrá el mismo número de elementos.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Acceda a la descripción del vértice pasada en [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La descripción del vértice describe el diseño de los búferes de vértices de la malla.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Determina si un rayo forma una intersección con esta malla.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina si un rayo forma una intersección con un subconjunto de esta malla.<br/>                                                                                                                                                                                                                                                                |
| [**Optimización**](id3dx10mesh-optimize.md)                                                 | Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Establecer los datos de adyacencia de la malla.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Establezca los datos de atributo de la malla.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Establecer los datos de índice de la malla.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Establezca los datos de representación del punto para la malla.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Establezca los datos de vértices en uno de los búferes de vértices de la malla.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Para obtener la interfaz ID3DX10Mesh, llame a [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
