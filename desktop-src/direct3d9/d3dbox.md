---
description: Define un volumen.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estructura D3DBOX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805518"
---
# <a name="d3dbox-structure"></a>D3DBOX (estructura)

Define un volumen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Left**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del lado izquierdo del cuadro en el eje X.

</dd> <dt>

**Top** (Principales)
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte superior del cuadro en el eje Y.

</dd> <dt>

**Right**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del lado derecho del cuadro en el eje X.

</dd> <dt>

**Bottom**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte inferior del cuadro en el eje Y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte delantera del cuadro en el eje Z.

</dd> <dt>

**Atrás**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte posterior del cuadro en el eje Z.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**D3DBOX incluye** los bordes izquierdo, superior y frontal; sin embargo, no se incluyen los bordes derecho, inferior y posterior. Por ejemplo, un cuadro que tiene 100 unidades de ancho y comienza en 0 (por lo tanto, incluidos los puntos hasta 99 incluidos) se expresaría con un valor de 0 para el miembro Left y un valor de 100 para el miembro Right. Tenga en cuenta que no se usa un valor de 99 para el miembro Right.

Las restricciones de ordenación lateral observadas para **D3DBOX** se encuentran de izquierda a derecha, de arriba abajo y de delante hacia atrás.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
