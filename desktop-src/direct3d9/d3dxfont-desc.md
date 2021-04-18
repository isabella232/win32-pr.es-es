---
description: Define los atributos de una fuente.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC estructura (D3dx9core. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721457"
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



## <a name="members"></a>Miembros

<dl> <dt>

**Height**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto, en unidades lógicas, de la celda de caracteres o carácter de la fuente.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho, en unidades lógicas, de caracteres de la fuente.

</dd> <dt>

**Peso**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de la fuente en el intervalo comprendido entre 0 y 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de MIP solicitados. Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa. Si el valor es 1, el espacio de textura se asigna de forma idéntica al espacio de la pantalla.

</dd> <dt>

**Cursiva**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Establézcalo en **true** para una fuente en cursiva.

</dd> <dt>

**CharSet**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Juego de caracteres.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisión de salida. La precisión de salida define el grado en que la salida debe coincidir con el alto de fuente, el ancho, la orientación de carácter, el escape, el paso y el tipo de fuente solicitados.

</dd> <dt>

**Quality**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Calidad de salida.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

El paso y la familia de la fuente.

</dd> <dt>

**FaceName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Una cadena o caracteres terminados en null que especifican el nombre del tipo de letra de la fuente. La longitud de la cadena no debe superar los 32 caracteres, incluido el carácter nulo de terminación. Si FaceName es una cadena vacía, se utilizará la primera fuente que coincida con los demás atributos especificados. Si la configuración del compilador requiere Unicode, el tipo de datos TCHAR se resuelve como WCHAR; de lo contrario, el tipo de datos se resuelve como CHAR. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina el tipo de estructura. Si se define Unicode, el \_ tipo de estructura D3DXFONT desc se resuelve como D3DXFONT \_ DESCW; de lo contrario, el tipo de estructura se resuelve como un D3DXFONT \_ Desca.

Los valores posibles de los miembros anteriores se proporcionan en la estructura de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) de GDI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
