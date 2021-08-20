---
description: Describe las definiciones de preprocesador utilizadas por un objeto de efecto.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Estructura D3DXMACRO (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: fa78c69ffe0c25b66e73da6fd9139c3b1f69661e5237c3c03e4dd2d8a377461d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095952"
---
# <a name="d3dxmacro-structure"></a>D3DXMACRO (estructura)

Describe las definiciones de preprocesador utilizadas por un objeto de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre del preprocesador.

</dd> <dt>

**Definición**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de definición.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar **D3DXMACRO** en más de una línea, antefija cada nuevo carácter de línea con una barra diagonal inversa (como una \# definición en el lenguaje C). Por ejemplo:


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Observe los tres caracteres de barra diagonal inversa al final de la línea. Los dos primeros son necesarios para generar una única \\ "", seguida del carácter de nueva línea \\ "n". Opcionalmente, es posible que también quiera finalizar las líneas mediante \\ \\ \\ "r \\ n".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
