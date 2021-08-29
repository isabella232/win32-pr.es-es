---
description: Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: Método ID3DXFont::P reloadText (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 874b2d6106a7dcbfb8992a8677a28841f7d44e8b1512c6258b7e3bef45770eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629875"
---
# <a name="id3dxfontpreloadtext-method"></a>Método ID3DXFont::P reloadText

Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***

Puntero a una cadena de caracteres que se va a cargar en la memoria de vídeo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR; De lo contrario, el tipo de datos se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Número de caracteres de la cadena de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve como PreloadTextW. De lo contrario, la llamada de función se resuelve como PreloadTextA porque se usan cadenas ANSI.

Este método genera texturas que contienen glifos que representan el texto de entrada. Los glifos se dibujan como una serie de triángulos.

El texto no se representará en el dispositivo; Todavía se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar el texto. Sin embargo, al cargar previamente texto en la memoria de vídeo, **DrawText** usará considerablemente menos recursos de CPU.

Este método convierte internamente caracteres en glifos mediante la función GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
