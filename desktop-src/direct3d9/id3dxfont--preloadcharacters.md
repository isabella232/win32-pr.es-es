---
description: Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: Método ID3DXFont::P reloadCharacters (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565933"
---
# <a name="id3dxfontpreloadcharacters-method"></a>Método ID3DXFont::P reloadCharacters

Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*En primer lugar* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del primer carácter que se va a cargar en la memoria de vídeo.

</dd> <dt>

*Último* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del último carácter que se va a cargar en la memoria de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Este método genera texturas que contienen glifos que representan los caracteres de entrada. Los glifos se dibujan como una serie de triángulos.

Los caracteres no se representarán en el dispositivo; Todavía se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar los caracteres. Sin embargo, al cargar previamente caracteres en la memoria de vídeo, **DrawText** usará considerablemente menos recursos de CPU.

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

 

 
