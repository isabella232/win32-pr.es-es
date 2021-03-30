---
description: Define las operaciones que se deben realizar en los vértices como preparación para la limpieza de malla.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeración D3DXCLEANTYPE (D3dx9mesh. h)
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
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280363"
---
# <a name="d3dxcleantype-enumeration"></a>Enumeración D3DXCLEANTYPE

Define las operaciones que se deben realizar en los vértices como preparación para la limpieza de malla.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**
</dt> <dd>

Mezclar triángulos que compartan los mismos índices de vértices pero que tengan caras normales que señalen a direcciones opuestas (triángulos hacia delante). A menos que los triángulos no se dividan agregando un vértice replicado, los datos de proximidad de la malla de los dos triángulos pueden entrar en conflicto.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ pajaritas**
</dt> <dd>

Si un vértice es el vértice de dos ventiladores de triángulo (una pajarita) y las operaciones de malla afectan a uno de los ventiladores, divida el vértice compartido en dos nuevos vértices. Las Pajaritas pueden causar problemas en operaciones como la simplificación de malla que quitan vértices, ya que la eliminación de un vértice afecta a dos conjuntos distintos de triángulos.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN de la \_ piel**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de malla de configuración de la piel.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Optimización de D3DXCLEAN \_**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de optimización de malla.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplificación de D3DXCLEAN**
</dt> <dd>

Use esta marca para evitar bucles infinitos durante las operaciones de simplificación de malla.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




