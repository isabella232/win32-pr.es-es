---
description: Dibuja texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont::D método rawText (D3dx9core. h)
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
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280312"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont::D método rawText

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

*pSprite* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Puntero a un objeto [**ID3DXSprite**](id3dxsprite.md) que contiene la cadena. Puede ser **null**, en cuyo caso Direct3D presentará la cadena con su propio objeto Sprite. Para mejorar la eficacia, se debe especificar un objeto Sprite si se va a llamar a **DrawText** más de una vez en una fila.

</dd> <dt>

*pString* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que se va a dibujar. Si el parámetro Count es-1, la cadena debe terminar en NULL.

</dd> <dt>

*Recuento* \[ de\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Especifica el número de caracteres de la cadena. Si Count es-1, se supone que el parámetro pString es un puntero a una cadena terminada en NULL y **DrawText** calcula el recuento de caracteres automáticamente.

</dd> <dt>

*pRect* \[ de\]
</dt> <dd>

Tipo: **[ **LPRECT**](../winprog/windows-data-types.md)**

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto. El valor de la coordenada del lado derecho del rectángulo debe ser mayor que el del lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

</dd> <dt>

*Formato* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el método para dar formato al texto. Puede ser cualquier combinación de los siguientes valores:



| Value                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**\_inferior DT**</dt> </dl>             | Justifica el texto en la parte inferior del rectángulo. Este valor se debe combinar con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | Determina el ancho y el alto del rectángulo. Si hay varias líneas de texto, **DrawText** usa el ancho del rectángulo señalado por el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto. Si solo hay una línea de texto, **DrawText** modifica el lado derecho del rectángulo de modo que delimita el último carácter de la línea. En cualquier caso, **DrawText** devuelve el alto del texto con formato, pero no dibuja el texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**\_Centro DT**</dt> </dl>             | Centra el texto horizontalmente en el rectángulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ EXPANDTABS**</dt> </dl> | Expande los caracteres de tabulación. El número de caracteres predeterminado por tabulación es ocho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT a la \_ izquierda**</dt> </dl>                   | Alinea el texto a la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOclip**</dt> </dl>             | Dibuja sin recortes. **DrawText** es algo más rápido cuando \_ se usa DT noclip.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**\_derecho DT**</dt> </dl>                | Alinea el texto a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | Muestra texto en orden de lectura de derecha a izquierda para el texto bidireccional cuando se selecciona una fuente hebreo o árabe. El orden de lectura predeterminado para todo el texto es de izquierda a derecha.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ SINGLELINE**</dt> </dl> | Muestra texto solo en una sola línea. Los retornos de carro y los saltos de línea no interrumpen la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**\_superior DT**</dt> </dl>                      | Texto que justifica la parte superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**\_vCenter DT**</dt> </dl>          | Centra el texto verticalmente (solo una línea).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WORDBREAK**</dt> </dl>    | Rompe las palabras. Las líneas se dividen automáticamente entre palabras si una palabra se extiende más allá del borde del rectángulo especificado por el parámetro pRect. Una secuencia de retorno de carro/avance de línea también rompe la línea.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Color* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Color del texto. Para obtener más información, vea [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Si la función se ejecuta correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si \_ se especifica dt vCenter o DT \_ Bottom, el valor devuelto es el desplazamiento de pRect (superior a la parte inferior) del texto dibujado. Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Los parámetros de este método son muy similares a los de la función [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) de GDI.

Este método admite cadenas ANSI y Unicode.

Se debe llamar a este método dentro de un [**BeginScene**](/windows/desktop/api) ... Bloque [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) . La única excepción es cuando una aplicación llama a **DrawText** con DT \_ CALCRECT para calcular el tamaño de un bloque de texto determinado.

A menos \_ que se use el formato DT noclip, este método recorta el texto para que no aparezca fuera del rectángulo especificado. Se supone que todo el formato tiene varias líneas a menos que \_ se especifique el formato DT SINGLELINE.

Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente menor.

Este método solo admite fuentes cuyo escape y orientación son cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
