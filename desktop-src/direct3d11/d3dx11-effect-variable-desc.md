---
title: D3DX11_EFFECT_VARIABLE_DESC estructura (D3dx11effect. h)
description: Describe una variable de efecto.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998694"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>D3DX11 de la variable de efecto de la \_ \_ \_ estructura DESC

Describe una variable de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de esta variable, anotación o miembro de estructura.

</dd> <dt>

**Semántica**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Cadena semántica de esta variable o miembro de estructura (NULL para las anotaciones o si no está presente).

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Marcas opcionales para las variables de efecto.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotaciones en esta variable (siempre es 0 para las anotaciones).

</dd> <dt>

**BufferOffset**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Desplazamiento en que contiene CBuffer o tbuffer (siempre es 0 para las anotaciones o variables que no están en búferes de constantes).

</dd> <dt>

**ExplicitBindPoint**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Se usa si la variable se ha enlazado explícitamente mediante la palabra clave Register. Marque las marcas del \_ punto de enlace de variable de efecto de D3DX11 \_ \_ \_ \_ .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La \_ \_ variable de efecto D3DX11 \_ desc se usa con [**ID3DX11EffectVariable:: GetDesc**](id3dx11effectvariable-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

