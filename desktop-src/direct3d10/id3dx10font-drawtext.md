---
description: Dibujar texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: Método ID3DX10Font::D rawText (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303175"
---
# <a name="id3dx10fontdrawtext-method"></a>Método ID3DX10Font::D rawText

Dibujar texto con formato. Este método admite cadenas ANSI y Unicode.

## <a name="syntax"></a>Sintaxis


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSprite* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Puntero a un objeto ID3DX10Sprite que contiene la cadena que desea dibujar. Puede ser **NULL,** en cuyo caso Direct3D representará la cadena con su propio objeto sprite. Para mejorar la eficacia, se debe especificar un objeto sprite si se va a llamar a ID3DX10Font::D rawText más de una vez en una fila.

</dd> <dt>

*pString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que se dibujará. Si se define UNICODE, este tipo de parámetro se resuelve en un LPCWSTR; de lo contrario, el tipo se resuelve en un LPCSTR. Si el parámetro Count es -1, la cadena debe terminar **en NULL.**

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Número de caracteres de la cadena. Si Count es -1, se supone que el parámetro pString es un puntero a un sprite que contiene una cadena terminada en NULL e ID3DX10Font::D rawText calcula automáticamente el recuento de caracteres.

</dd> <dt>

*pRect* \[ En\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una [estructura RECT](/previous-versions//ms536136(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto. Al igual que con cualquier objeto RECT, el valor de coordenada del lado derecho del rectángulo debe ser mayor que el de su lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifique el método para dar formato al texto. Puede ser cualquier combinación de los valores siguientes:



| Elemento                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ BOTTOM<br/>             | Justificar el texto en la parte inferior del rectángulo. Este valor debe combinarse con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Diga a DrawText que calcule automáticamente el ancho y el alto del rectángulo en función de la longitud de la cadena que le diga que dibuje. Si hay varias líneas de texto, ID3DX10Font::D rawText usa el ancho del rectángulo al que apunta el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto. Si solo hay una línea de texto, ID3DX10Font::D rawText modifica el lado derecho del rectángulo para enlazar el último carácter de la línea. En cualquier caso, ID3DX10Font::D rawText devuelve el alto del texto con formato, pero no dibuja el texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>CENTRO DE \_ DT<br/>             | Centrar el texto horizontalmente en el rectángulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | Expanda los caracteres de tabulación. El número de caracteres predeterminado por tabulación es ocho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ LEFT<br/>                   | Alinee el texto a la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOCLIP<br/>             | Dibujar sin recorte. ID3DX10Font::D rawText es algo más rápido cuando se usa DT \_ NOCLIP.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ RIGHT<br/>                | Alinee el texto a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Mostrar texto en orden de lectura de derecha a izquierda para texto bidireccional cuando se selecciona una fuente árabe o hebreo. El orden de lectura predeterminado para todo el texto es de izquierda a derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE<br/> | Mostrar texto solo en una sola línea. Los retornos de carro y los avances de línea no rompen la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP<br/>                      | Texto de justificación superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER<br/>          | Centrar el texto verticalmente (solo una línea).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | Palabras de interrupción. Las líneas se divide automáticamente entre palabras si una palabra se extendería más allá del borde del rectángulo especificado por el parámetro pRect. Una secuencia de retorno de carro o avance de línea también interrumpe la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Color del texto. Vea [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Si la función se realiza correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si se especifica DT VCENTER o DT BOTTOM, el valor devuelto es el desplazamiento desde pRect (de arriba a \_ \_ abajo) del texto dibujado. Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Los parámetros de este método son muy similares a los de la [función DrawText de GDI.](/previous-versions//ms533909(v=vs.85))

Este método admite cadenas ANSI y Unicode.

A menos que se utilice el formato DT NOCLIP, este método recorta el texto para que no aparezca \_ fuera del rectángulo especificado. Se supone que todo el formato tiene varias líneas, a menos que se especifique el formato DT \_ SINGLELINE.

Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente más pequeña.

Este método solo admite fuentes cuyo escape y orientación son cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
