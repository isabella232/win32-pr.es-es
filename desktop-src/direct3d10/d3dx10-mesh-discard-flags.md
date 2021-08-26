---
description: Especifica qué fragmentos de datos de malla se descartarán del dispositivo. Se usa con ID3DX10Mesh::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: D3DX10_MESH_DISCARD_FLAGS enumeración (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989475"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>Enumeración D3DX10 \_ MESH \_ DISCARD \_ FLAGS

Especifica qué fragmentos de datos de malla se descartarán del dispositivo. Se usa [**con ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**BÚFER DE ATRIBUTO \_ DE DESCARTE DE MALLA D3DX10 \_ \_ \_**
</dt> <dd>

Descarte el búfer de atributo.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**TABLA DE ATRIBUTOS DE DESCARTE DE MALLA D3DX10 \_ \_ \_ \_**
</dt> <dd>

Descarte la tabla de atributos.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ MESH \_ DISCARD \_ POINTREPS**
</dt> <dd>

Descarte el búfer de representaciones de puntero.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**ADYACENCIA DE DESCARTE DE MALLA D3DX10 \_ \_ \_**
</dt> <dd>

Descarte el búfer de adyacencia.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ MESH \_ DESCARTA \_ BÚFERES DE \_ DISPOSITIVO**
</dt> <dd>

Descarte los búferes confirmados en el dispositivo [**(con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




