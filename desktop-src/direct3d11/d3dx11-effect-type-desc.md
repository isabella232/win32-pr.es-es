---
title: D3DX11_EFFECT_TYPE_DESC estructura (D3dx11effect.h)
description: Describe un tipo de variable de efecto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC estructura direct3D 11
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
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989965"
---
# <a name="d3dx11_effect_type_desc-structure"></a>D3DX11 \_ EFFECT \_ TYPE \_ DESC (Estructura DESC)

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

Nombre del tipo, por ejemplo"float4" o "MyStruct".

</dd> <dt>

**Clase**
</dt> <dd>

Tipo: **[ **D3D10 \_ SHADER \_ VARIABLE \_ CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

La clase variable (vea [**D3D10 \_ SHADER \_ VARIABLE \_ CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **TIPO DE VARIABLE DE \_ SOMBREADOR \_ \_ D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Tipo de variable (vea [**D3D10 \_ SHADER \_ VARIABLE \_ TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de este tipo (0 si no es una matriz).

</dd> <dt>

**Miembros**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de miembros (0 si no es una estructura).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de filas de este tipo (0 si no es una primitiva numérica).

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de columnas de este tipo (0 si no es una primitiva numérica).

</dd> <dt>

**PackedSize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes necesarios para representar este tipo de datos, cuando se empaquetan estrechamente.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes ocupados por este tipo de datos, cuando se establecen en un búfer constante.

</dd> <dt>

**Paso**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes que se buscarán entre elementos, cuando se dispone en un búfer constante.

</dd> </dl>

## <a name="remarks"></a>Comentarios

D3DX11 \_ EFFECT \_ TYPE \_ DESC se usa [ **con ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

