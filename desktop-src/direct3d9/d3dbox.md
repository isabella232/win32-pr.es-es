---
description: Define un volumen.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estructura D3DBOX (D3D9Types. h)
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
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280269"
---
# <a name="d3dbox-structure"></a>Estructura D3DBOX

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del lado izquierdo del cuadro en el eje x.

</dd> <dt>

**Top** (Principales)
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte superior del cuadro en el eje y.

</dd> <dt>

**Right**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del lado derecho del cuadro en el eje x.

</dd> <dt>

**Bottom**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición de la parte inferior del cuadro en el eje y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del anverso del cuadro en el eje z.

</dd> <dt>

**Atrás**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posición del fondo del cuadro en el eje z.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**D3DBOX** incluye los bordes izquierdo, superior y frontal; sin embargo, no se incluyen los bordes derecho, inferior y trasero. Por ejemplo, un cuadro de 100 unidades de ancho y comienza en 0 (por lo tanto, incluidos los puntos hasta 99) se expresaría con un valor de 0 para el miembro izquierdo y un valor de 100 para el miembro de la derecha. Tenga en cuenta que el valor 99 no se utiliza para el miembro de la derecha.

Las restricciones en la ordenación lateral observadas para **D3DBOX** son de izquierda a derecha, de arriba a abajo y de delante a atrás.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
