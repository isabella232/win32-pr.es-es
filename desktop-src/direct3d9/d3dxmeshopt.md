---
description: Especifica el tipo de optimización de malla que se va a realizar.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeración D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698239"
---
# <a name="d3dxmeshopt-enumeration"></a>Enumeración D3DXMESHOPT

Especifica el tipo de optimización de malla que se va a realizar.

## <a name="syntax"></a>Sintaxis


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**
</dt> <dd>

Reordena las caras para quitar los vértices y caras sin usar.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Reordena las caras para optimizar menos cambios de estado de agrupación de atributos y ID3DXBaseMesh mejorado: el rendimiento de la [**:D rawsubset**](id3dxbasemesh--drawsubset.md) .

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Reordena las caras para aumentar la tasa de aciertos de caché de los vértices.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Reordena las caras para maximizar la longitud de los triángulos adyacentes.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Optimizar solo las caras; no optimice los vértices.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Mientras se ordena el atributo, no divida los vértices que se comparten entre los grupos de atributos.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Afecta al tamaño de la caché de vértices. El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en el hardware heredado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las \_ marcas de optimización D3DXMESHOPT STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE se excluyen mutuamente.

La marca D3DXMESHOPT SHAREVB se ha \_ quitado de esta enumeración. \_ \_ En su lugar, use D3DXMESH VB Share, en [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
