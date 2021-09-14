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
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063801"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>Enumeración D3DX10 \_ MESH \_ DISCARD \_ FLAGS

Especifica qué fragmentos de datos de malla se descartarán del dispositivo. Se usa [**con ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**BÚFER DE ATRIBUTO DE DESCARTE DE MALLA D3DX10 \_ \_ \_ \_**
</dt> <dd>

Descarte el búfer de atributos.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**TABLA DE ATRIBUTOS DE DESCARTE DE MALLA D3DX10 \_ \_ \_ \_**
</dt> <dd>

Descarte la tabla de atributos.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ MESH \_ DISCARD \_ POINTREPS**
</dt> <dd>

Descarte el búfer de réplicas de puntero.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ MESH \_ DISCARD \_ ADJACENCY**
</dt> <dd>

Descarte el búfer de adyacencia.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**BÚFERES DE DISPOSITIVO DE DESCARTE DE MALLA D3DX10 \_ \_ \_ \_**
</dt> <dd>

Descarte los búferes confirmados en el dispositivo [**(con ID3DX10Mesh::CommitToDevice).**](id3dx10mesh-committodevice.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




