---
description: Dibujar texto con formato. Este método admite cadenas ANSI y Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font::D método rawText (D3DX10. h)
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
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698266"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font::D método rawText

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

*pSprite* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Puntero a un objeto ID3DX10Sprite que contiene la cadena que desea dibujar. Puede ser **null**, en cuyo caso Direct3D presentará la cadena con su propio objeto Sprite. Para mejorar la eficacia, se debe especificar un objeto Sprite si ID3DX10Font::D rawText se va a llamar más de una vez en una fila.

</dd> <dt>

*pString* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que se va a dibujar. Si se define Unicode, este tipo de parámetro se resuelve en un LPCWSTR; de lo contrario, el tipo se resuelve como un LPCSTR. Si el parámetro Count es-1, la cadena debe terminar en **null** .

</dd> <dt>

*Recuento* \[ de\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Número de caracteres de la cadena. Si Count es-1, se supone que el parámetro pString es un puntero a un Sprite que contiene una cadena terminada en NULL y ID3DX10Font::D rawText calcula el recuento de caracteres automáticamente.

</dd> <dt>

*pRect* \[ de\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una estructura [Rect](/previous-versions//ms536136(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto. Como con cualquier objeto RECT, el valor de la coordenada del lado derecho del rectángulo debe ser mayor que el del lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

</dd> <dt>

*Formato* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifique el método para dar formato al texto. Puede ser cualquier combinación de los siguientes valores:



| Elemento                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>\_inferior DT<br/>             | Justifique el texto en la parte inferior del rectángulo. Este valor se debe combinar con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Indique a DrawText que calcule automáticamente el ancho y el alto del rectángulo en función de la longitud de la cadena que indica que se va a dibujar. Si hay varias líneas de texto, ID3DX10Font::D rawText usa el ancho del rectángulo al que apunta el parámetro pRect y extiende la base del rectángulo para enlazar la última línea de texto. Si solo hay una línea de texto, ID3DX10Font::D rawText modifica el lado derecho del rectángulo de modo que delimita el último carácter de la línea. En cualquier caso, ID3DX10Font::D rawText devuelve el alto del texto con formato, pero no dibuja el texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>\_Centro DT<br/>             | Centrar el texto horizontalmente en el rectángulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | Expandir caracteres de tabulación. El número de caracteres predeterminado por tabulación es ocho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT a la \_ izquierda<br/>                   | Alinear el texto a la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip<br/>             | Dibuja sin recortes. ID3DX10Font::D rawText es algo más rápido cuando \_ se usa DT noclip.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>\_derecho DT<br/>                | Alinear el texto a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Muestra texto en orden de lectura de derecha a izquierda para el texto bidireccional cuando se selecciona una fuente hebreo o árabe. El orden de lectura predeterminado para todo el texto es de izquierda a derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE<br/> | Mostrar texto solo en una sola línea. Los retornos de carro y los saltos de línea no interrumpen la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>\_superior DT<br/>                      | Texto que justifica la parte superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_vCenter DT<br/>          | Centrar el texto verticalmente (solo una línea).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | Romper palabras. Las líneas se dividen automáticamente entre palabras si una palabra se extiende más allá del borde del rectángulo especificado por el parámetro pRect. Una secuencia de retorno de carro/avance de línea también rompe la línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Color* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Color del texto. Vea [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Si la función se ejecuta correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si \_ se especifica dt vCenter o DT \_ Bottom, el valor devuelto es el desplazamiento de pRect (superior a la parte inferior) del texto dibujado. Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Los parámetros de este método son muy similares a los de la función [DrawText de GDI](/previous-versions//ms533909(v=vs.85)) .

Este método admite cadenas ANSI y Unicode.

A menos \_ que se use el formato DT noclip, este método recorta el texto para que no aparezca fuera del rectángulo especificado. Se supone que todo el formato tiene varias líneas a menos que \_ se especifique el formato DT SINGLELINE.

Si la fuente seleccionada es demasiado grande para el rectángulo, este método no intenta sustituir una fuente menor.

Este método solo admite fuentes cuyo escape y orientación son cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
