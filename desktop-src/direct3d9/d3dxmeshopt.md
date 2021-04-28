---
description: 'Enumeración D3DXMESHOPT: especifica el tipo de optimización de malla que se va a realizar.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeración D3DXMESHOPT (D3dx9mesh.h)
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
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114353"
---
# <a name="d3dxmeshopt-enumeration"></a>Enumeración D3DXMESHOPT

Especifica el tipo de optimización de malla que se va a realizar.

## <a name="syntax"></a>Syntax


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

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**
</dt> <dd>

Reordena las caras para quitar los vértices y las caras que no se usan.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Reordena las caras para optimizar para obtener menos cambios de estado de agrupación de atributos y un rendimiento [**mejorado de ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md)

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Reordena las caras para aumentar la tasa de aciertos de caché de las cachés de vértices.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Reordena las caras para maximizar la longitud de los triángulos adyacentes.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Optimice solo las caras; no optimice los vértices.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Durante la ordenación de atributos, no divida los vértices que se comparten entre grupos de atributos.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Afecta al tamaño de la caché de vértices. El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en hardware heredado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las marcas de optimización D3DXMESHOPT \_ STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE son mutuamente excluyentes.

La marca SHAREVB D3DXMESHOPT \_ se ha quitado de esta enumeración. Use D3DXMESH \_ VB SHARE en su \_ lugar, en [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
