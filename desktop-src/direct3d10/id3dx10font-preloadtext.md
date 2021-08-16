---
description: Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: Método ID3DX10Font::P reloadText (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 23c7a3a8ce8ed3534a7369f167ce1045d200cbaeea1aa80653e05412ffa978e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302850"
---
# <a name="id3dx10fontpreloadtext-method"></a>Método ID3DX10Font::P reloadText

Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena de caracteres que se va a cargar en la memoria de vídeo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR; De lo contrario, el tipo de datos se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Número de caracteres de la cadena de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve como PreloadTextW. De lo contrario, la llamada de función se resuelve como PreloadTextA porque se usan cadenas ANSI.

Este método genera texturas que contienen glifos que representan el texto de entrada. Los glifos se dibujan como una serie de triángulos.

El texto no se representará en el dispositivo; Todavía se debe llamar a ID3DX10Font::D rawText para representar el texto. Sin embargo, al cargar previamente texto en la memoria de vídeo, ID3DX10Font::D rawText usará considerablemente menos recursos de CPU.

Este método convierte internamente caracteres en glifos mediante la función GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).

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

 

 
