---
description: Define los atributos de una fuente.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC estructura (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567944"
---
# <a name="d3dxfont_desc-structure"></a>D3DXFONT \_ DESC (estructura)

Define los atributos de una fuente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Members

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

Número de niveles de mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mip completa. Si el valor es 1, el espacio de textura se asigna de forma idéntica al espacio de pantalla.

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

Precisión de salida. La precisión de salida define el grado de coincidencia de la salida con el alto de fuente, el ancho, la orientación de caracteres, el escape, el tono y el tipo de fuente solicitados.

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

**FaceName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Cadena terminada en NULL o caracteres que especifica el nombre del tipo de letra de la fuente. La longitud de la cadena no debe superar los 32 caracteres, incluido el carácter nulo final. Si FaceName es una cadena vacía, se usará la primera fuente que coincida con los demás atributos especificados. Si la configuración del compilador requiere Unicode, el tipo de datos TCHAR se resuelve en WCHAR; De lo contrario, el tipo de datos se resuelve como CHAR. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina el tipo de estructura. Si se define Unicode, el tipo de estructura D3DXFONT DESC se resuelve en D3DXFONT DESCW; de lo contrario, el tipo de estructura se resuelve como \_ \_ D3DXFONT \_ DESCA.

Los valores posibles de los miembros anteriores se dan en la estructura [**LOGFONT de**](/windows/win32/api/wingdi/ns-wingdi-logfonta) GDI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
