---
description: Características del material de la transferencia Radiance (PRT) precalculada del armónico (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estructura D3DXSHMATERIAL (D3dx9mesh. h)
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
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717739"
---
# <a name="d3dxshmaterial-structure"></a>Estructura D3DXSHMATERIAL

Características del material de la transferencia Radiance (PRT) precalculada del armónico (SH).

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

Difusión albedo de la superficie. Este valor se omite si el objeto es un reflejo.

</dd> <dt>

**bMirror**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Debe establecerse en **false**.

</dd> <dt>

**bSubSurf**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Establézcalo en **true** para habilitar la dispersión de subsuperficies; cualquier objeto que realiza la dispersión de subsuperficies no puede ser un reflejo.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

El Índice relativo de la refracción es la proporción entre dos índices absolutos de la refracción. Un índice de refracción es la proporción entre el seno del ángulo de la incidencia y el seno del ángulo de la refracción.

</dd> <dt>

**Absorbe**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

El coeficiente de absorción es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación ligera en un medio participante.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

El coeficiente de dispersión reducido es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación ligera en un medio participante.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las escenas no espectrales usan el canal rojo de los materiales en lugar del valor de luminancia.

Para obtener más información acerca de PRT, consulte:

-   Jensen, Henrik Wann, et al. SIGGRAPH: un modelo práctico para el transporte de luz de subsuperficie, 2001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
