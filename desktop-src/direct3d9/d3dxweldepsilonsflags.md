---
description: Opciones para la colaboración entre vértices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumeración D3DXWELDEPSILONSFLAGS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963736"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>Enumeración D3DXWELDEPSILONSFLAGS

Opciones para la colaboración entre vértices.

## <a name="syntax"></a>Sintaxis


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONSALL \_**
</dt> <dd>

Reúne todos los vértices que se encuentran en la misma ubicación. El uso de esta marca evita una comparación de epsilón entre los componentes de vértice.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ HISTOGRAMAPARTIALMATCHES**
</dt> <dd>

Si un componente de vértice determinado está dentro del epsilón, modifique los vértices coincidentes parcialmente para que ambos componentes sean idénticos. Si todos los componentes son iguales, quite uno de los vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**
</dt> <dd>

Indica a la herramienta que permita solo las modificaciones en los vértices y no la eliminación. Esta marca solo es válida si se establece D3DXWELDEPSILONS \_ HISTOGRAMPARTIALMATCHES. Resulta útil modificar los vértices para que sean iguales, pero no para permitir que se quiten los vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**
</dt> <dd>

Indica a la clase que no divida los vértices que están en grupos de atributos independientes. Cuando se llama al método [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) con la marca D3DXMESHOPT ATTRSORT, también se establecerá la marca \_ D3DXMESHOPT \_ DONOTSPLIT. Establecer esta marca puede ralentizar el procesamiento de vértices de software.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




