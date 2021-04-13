---
description: Opciones de soldadura entre vértices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumeración D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362607"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>Enumeración D3DXWELDEPSILONSFLAGS

Opciones de soldadura entre vértices.

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

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**
</dt> <dd>

Soldadura juntas todos los vértices que se encuentran en la misma ubicación. El uso de esta marca evita una comparación de épsilon entre los componentes de vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**
</dt> <dd>

Si un componente de vértice determinado está en épsilon, modifique los vértices parcialmente coincidentes para que ambos componentes sean idénticos. Si todos los componentes son iguales, Quite uno de los vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**
</dt> <dd>

Indica a la soldadura que solo permita modificaciones en los vértices y no en la eliminación. Esta marca solo es válida si \_ se establece D3DXWELDEPSILONS WELDPARTIALMATCHES. Resulta útil modificar los vértices para que sean iguales, pero no para permitir que se quiten los vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**
</dt> <dd>

Indica a la soldadura que no divida los vértices que se encuentran en grupos de atributos independientes. Cuando se llama al método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con la \_ marca ATTRSORT de D3DXMESHOPT, \_ también se establecerá la marca D3DXMESHOPT DONOTSPLIT. La configuración de esta marca puede ralentizar el procesamiento de vértices de software.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




