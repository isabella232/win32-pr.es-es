---
description: Especifica el tipo de optimización de malla que se va a realizar.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumeración D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362711"
---
# <a name="d3dx10_meshopt-enumeration"></a>\_Enumeración de D3DX10 MESHOPT

Especifica el tipo de optimización de malla que se va a realizar.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**
</dt> <dd>

Reordena las caras para quitar los vértices y caras sin usar.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ Sort**
</dt> <dd>

Reordena las caras para optimizar menos cambios de estado de agrupación de atributos y rendimiento de DrawSubset mejorado.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ Vertex \_ Cache**
</dt> <dd>

Reordena las caras para aumentar la tasa de aciertos de caché de los vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Reordenación de D3DX10 \_ MESHOPT \_ \_**
</dt> <dd>

Reordena las caras para maximizar la longitud de los triángulos adyacentes.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignore \_ VERTS**
</dt> <dd>

Optimizar solo las caras; no optimice los vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ \_ no se \_ divide**
</dt> <dd>

Mientras se ordena el atributo, no divida los vértices que se comparten entre los grupos de atributos.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**\_Independiente del \_ dispositivo \_ MESHOPT de D3DX10**
</dt> <dd>

Afecta al tamaño de la caché de vértices. El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en el hardware heredado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las \_ marcas de optimización D3DXMESHOPT STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE se excluyen mutuamente.

La marca D3DXMESHOPT SHAREVB se ha \_ quitado de esta enumeración. \_ \_ En su lugar, use D3DXMESH VB Share, en D3DXMESH.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




