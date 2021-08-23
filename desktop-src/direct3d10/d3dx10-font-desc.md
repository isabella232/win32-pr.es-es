---
description: Define atributos de fuente.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634955"
---
# <a name="d3dx10_font_desc-structure"></a>D3DX10 \_ FONT \_ DESC (estructura)

Define atributos de fuente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Height**
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto, en unidades lógicas, de la celda de caracteres o el carácter de la fuente.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho, en unidades lógicas, de caracteres en la fuente.

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de la fuente en el intervalo de 0 a 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de asignación mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mipmap completa. Si el valor es 1, el espacio de textura se asigna de forma idéntica al espacio de pantalla.

</dd> <dt>

**Cursiva**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Establezca en **TRUE para** una fuente cursiva.

</dd> <dt>

**Charset**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Juego de caracteres.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisión de salida. La precisión de salida define la precisión con la que la salida debe coincidir con el alto de fuente, el ancho, la orientación de caracteres, el escape, el tono y el tipo de fuente solicitados.

</dd> <dt>

**Quality**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Calidad de salida.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tono y familia de la fuente.

</dd> <dt>

**FaceName \[ LF \_ FACESIZE\]**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Cadena terminada en NULL que especifica el nombre del tipo de letra de la fuente. La longitud de la cadena no debe superar los 32 caracteres, incluido el carácter **NULL final.** Si FaceName es una cadena vacía, se usará la primera fuente que coincida con los demás atributos especificados. Si la configuración del compilador requiere Unicode, el tipo de datos TCHAR se resuelve en WCHAR; De lo contrario, el tipo de datos se resuelve en CHAR. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina el tipo de estructura. Si se define Unicode, el tipo de estructura DESC FONT DESC de D3DX10 se resuelve en D3DX10 FONT DESCW; de lo contrario, el tipo de estructura se resuelve en un \_ \_ \_ \_ \_ \_ DESCA FONT D3DX10.

Los valores posibles de los miembros anteriores se dan en la estructura [LOGFONT de](/previous-versions//ms533931(v=vs.85)) GDI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
