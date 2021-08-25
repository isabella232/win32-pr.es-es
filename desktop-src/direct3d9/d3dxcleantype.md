---
description: Define las operaciones que se realizan en los vértices como preparación para la limpieza de malla.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeración D3DXCLEANTYPE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894115"
---
# <a name="d3dxcleantype-enumeration"></a>D3DXCLEANTYPE (enumeración)

Define las operaciones que se realizan en los vértices como preparación para la limpieza de malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**
</dt> <dd>

Combinar triángulos que comparten los mismos índices de vértice pero que tienen normales faciales que apuntan en direcciones opuestas (triángulos orientados hacia atrás). A menos que los triángulos no se divida agregando un vértice replicado, los datos de adyacencia de malla de los dos triángulos pueden estar en conflicto.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

Si un vértice es el vértice de dos ventiladores de triángulo (una arco) y las operaciones de malla afectarán a uno de los ventiladores, divida el vértice compartido en dos vértices nuevos. Las arcos pueden causar problemas para operaciones como la simplificación de mallas que quitan vértices, ya que la eliminación de un vértice afecta a dos conjuntos distintos de triángulos.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ SKINNING**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de malla de configuración de desplazamiento.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**OPTIMIZACIÓN \_ D3DXCLEAN**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de optimización de malla.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**SIMPLIFICACIÓN DE \_ D3DXCLEAN**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de simplificación de malla.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




