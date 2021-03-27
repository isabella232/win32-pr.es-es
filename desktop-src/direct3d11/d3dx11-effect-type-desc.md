---
title: D3DX11_EFFECT_TYPE_DESC estructura (D3dx11effect. h)
description: Describe un tipo de variable de efecto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914798"
---
# <a name="d3dx11_effect_type_desc-structure"></a>Tipo de efecto de D3DX11 ( \_ \_ \_ estructura DESC)

Describe un tipo de variable de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TypeName**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre del tipo, por ejemplo "FLOAT4" o "@ struct".

</dd> <dt>

**Clase**
</dt> <dd>

Tipo: **[ **D3D10 \_ clase de \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

La clase variable (consulte [**\_ \_ \_ clase de variable de sombreador D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3D10 \_ tipo de \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

El tipo de variable (vea [**D3D10 (tipo de \_ \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de este tipo (0 si no es una matriz).

</dd> <dt>

**Miembros**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de miembros (0 si no es una estructura).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de filas de este tipo (0 si no es un primitivo numérico).

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de columnas de este tipo (0 si no es un primitivo numérico).

</dd> <dt>

**PackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes necesarios para representar este tipo de datos, cuando está estrechamente empaquetado.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes ocupado por este tipo de datos, cuando se dispone en un búfer de constantes.

</dd> <dt>

**STRI**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes que se van a buscar entre los elementos, cuando se disponen en un búfer de constantes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ Tipo de efecto D3DX11 \_ desc se usa con [ **ID3DX11EffectType:: GetDesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

