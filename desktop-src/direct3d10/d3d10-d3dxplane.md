---
description: 'Estructura D3DXPLANE (D3DX10Math.h): describe un plano.'
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estructura D3DXPLANE (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ccdc8644f63bdb048f6caa97ef635165a11a4473f549214410558583c8f807c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754265"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>Estructura D3DXPLANE (D3DX10Math.h)

Describe un plano.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Un**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente b del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente c del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente d del plano de recorte en la ecuación del plano general. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de la **estructura D3DXPLANE** toman la forma de la ecuación de plano general. Encajan en la ecuación del plano general para que el eje + por + dw + dw = 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
