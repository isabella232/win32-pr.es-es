---
description: Un búfer de malla es un búfer que contiene datos sobre una malla.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interfaz ID3DX10MeshBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2aeabcd6dd3cc711636d0e275f76ab48537953671559e244cf341e270783fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540159"
---
# <a name="id3dx10meshbuffer-interface"></a>Interfaz ID3DX10MeshBuffer

Un búfer de malla es un búfer que contiene datos sobre una malla. Puede contener uno de los cinco tipos diferentes de datos: datos de vértices, datos de índice, datos de adyacencia, datos de atributo o datos de punto de repetición. La estructura se usa para tener acceso a estos cinco datos a través de las cinco API siguientes: [**ID3DX10Mesh::GetVertexBuffer,**](id3dx10mesh-getvertexbuffer.md) [**ID3DX10Mesh::GetIndexBuffer,**](id3dx10mesh-getindexbuffer.md) [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)o [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Miembros

La **interfaz ID3DX10MeshBuffer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10MeshBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10MeshBuffer** tiene estos métodos.



| Método                                       | Descripción                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Obtiene el tamaño del búfer de malla, en bytes.<br/>                      |
| [**Mapa**](id3dx10meshbuffer-map.md)         | Obtenga un puntero a la memoria del búfer de malla para modificar su contenido.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Desamape un búfer.<br/>                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
