---
description: Dibuja texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: Método ID3DXFont::D rawText (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987425"
---
# <a name="id3dxfontdrawtext-method"></a>Método ID3DXFont::D rawText

Dibuja texto con formato. Este método admite cadenas ANSI y Unicode.

## <a name="syntax"></a>Sintaxis


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSprite* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Puntero a un [**objeto ID3DXSprite**](id3dxsprite.md) que contiene la cadena. Puede ser **NULL,** en cuyo caso Direct3D representará la cadena con su propio objeto sprite. Para mejorar la eficacia, se debe especificar un objeto sprite si se va a llamar a **DrawText** más de una vez en una fila.

</dd> <dt>

*pString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que se dibujará. Si el parámetro Count es -1, la cadena debe terminar en NULL.

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Especifica el número de caracteres de la cadena. Si Count es -1, se supone que el parámetro pString es un puntero a una cadena terminada en NULL y **DrawText** calcula automáticamente el recuento de caracteres.

</dd> <dt>

*pRect* \[ En\]
</dt> <dd>

Tipo: **[ **LPRECT**](../winprog/windows-data-types.md)**

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto. El valor de la coordenada del lado derecho del rectángulo debe ser mayor que el de su lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el método para dar formato al texto. Puede ser cualquier combinación de los valores siguientes:



| Value                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ BOTTOM**</dt> </dl>             | Justifica el texto en la parte inferior del rectángulo. Este valor debe combinarse con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | Determina el ancho y alto del rectángulo. Si hay varias líneas de texto, **DrawText** usa el ancho del rectángulo al que apunta el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto. Si solo hay una línea de texto, **DrawText** modifica el lado derecho del rectángulo para enlazar el último carácter de la línea. En cualquier caso, **DrawText** devuelve el alto del texto con formato, pero no dibuja el texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**CENTRO \_ DE DT**</dt> </dl>             | Centra el texto horizontalmente en el rectángulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ EXPANDTABS**</dt> </dl> | Expande los caracteres de tabulación. El número de caracteres predeterminado por tabulación es ocho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT \_ LEFT**</dt> </dl>                   | Alinea el texto a la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOCLIP**</dt> </dl>             | Dibuja sin recorte. **DrawText** es algo más rápido cuando se usa DT \_ NOCLIP.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT \_ RIGHT**</dt> </dl>                | Alinea el texto a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | Muestra texto en orden de lectura de derecha a izquierda para texto bidireccional cuando se selecciona una fuente en hebreo o árabe. El orden de lectura predeterminado para todo el texto es de izquierda a derecha.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ SINGLELINE**</dt> </dl> | Muestra texto solo en una sola línea. Los retornos de carro y los avances de línea no interrumpirán la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ TOP**</dt> </dl>                      | Texto que se justifica en la parte superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**DT \_ VCENTER**</dt> </dl>          | Centra el texto verticalmente (solo una línea).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WORDBREAK**</dt> </dl>    | Interrumpe las palabras. Las líneas se divide automáticamente entre palabras si una palabra se extendería más allá del borde del rectángulo especificado por el parámetro pRect. Una secuencia de retorno de carro/avance de línea también interrumpe la línea.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Color del texto. Para obtener más información, [**vea D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Si la función se realiza correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si se especifica DT VCENTER o DT BOTTOM, el valor devuelto es el desplazamiento desde pRect (de arriba a \_ \_ abajo) del texto dibujado. Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Los parámetros de este método son muy similares a los de la función [**DrawText de**](/windows/win32/api/winuser/nf-winuser-drawtext) GDI.

Este método admite cadenas ANSI y Unicode.

Se debe llamar a este método dentro de [**un beginScene**](/windows/desktop/api) ... [**Bloque EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) La única excepción es cuando una aplicación llama a **DrawText** con DT CALCRECT para calcular el \_ tamaño de un bloque de texto determinado.

A menos que se utilice el formato DT NOCLIP, este método recorta el texto para que no aparezca \_ fuera del rectángulo especificado. Se supone que todo el formato tiene varias líneas a menos que se especifique el \_ formato DT SINGLELINE.

Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente más pequeña.

Este método solo admite fuentes cuyo escape y orientación son cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
