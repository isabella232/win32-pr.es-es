---
description: Características del material de transferencia de radiancia precalutada (PRT) esférica (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estructura D3DXSHMATERIAL (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 4bfbf00c7d8654ad851ca8c691c9f028c09648219dbe76bb4ef07fe3b830e4d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849725"
---
# <a name="d3dxshmaterial-structure"></a>D3DXSHMATERIAL (estructura)

Características del material de transferencia de radiancia precalutada (PRT) esférica (SH).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Albedo difuso de la superficie. Este valor se omite si el objeto es un reflejo.

</dd> <dt>

**bMirror**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Debe establecerse en **FALSE.**

</dd> <dt>

**bSubSub**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Establezca en **TRUE para** habilitar la dispersión de subsuelo; cualquier objeto que realiza la dispersión de subsuelo no puede ser un reflejo.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

El índice relativo de retracción es la relación entre dos índices absolutos de retracción. Un índice de retracción es la proporción del seno del ángulo de la contención con el seno del ángulo de retracción.

</dd> <dt>

**Absorción**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

El coeficiente de absorción es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación de la luz en un medio participante.

</dd> <dt>

**Reducción de la seguridad**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

El coeficiente de dispersión reducido es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación de la luz en un medio participante.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las escenas no espectrales usan el canal rojo de los materiales en lugar del valor de luminosidad.

Para obtener más información sobre PRT, vea:

-   Seg, Vak Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
