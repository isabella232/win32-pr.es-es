---
description: Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: Método ID3DXFont::P reloadGlyphs (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea422a6e0b0ecfda6b4eb03a0636eb013d8c840c96cec6f1c482589de29f3c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563935"
---
# <a name="id3dxfontpreloadglyphs-method"></a>Método ID3DXFont::P reloadGlyphs

Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*En primer lugar* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del primer glifo que se va a cargar en la memoria de vídeo.

</dd> <dt>

*Último* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del último glifo que se va a cargar en la memoria de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Este método genera texturas que contienen los glifos de entrada. Los glifos se dibujan como una serie de triángulos.

Los glifos no se representarán en el dispositivo; Todavía se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar los glifos. Sin embargo, al cargar previamente glifos en la memoria de vídeo, **DrawText** usará considerablemente menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
