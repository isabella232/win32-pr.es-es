---
description: La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interfaz ID3DX10Font (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540351"
---
# <a name="id3dx10font-interface"></a>Interfaz ID3DX10Font

La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.

## <a name="members"></a>Miembros

La **interfaz ID3DX10Font** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Font** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10Font** tiene estos métodos.



| Método                                                     | Descripción                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dx10font-drawtext.md)                   | Dibujar texto con formato. Este método admite cadenas ANSI y Unicode.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Devuelve un identificador a un contexto de dispositivo de visualización (DC) que tiene la fuente establecida en él.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Obtenga una descripción del objeto de fuente actual.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Recupere el dispositivo Direct3D asociado al objeto de fuente.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Recuperar características de fuente.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Cargue una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.<br/> |



 

## <a name="remarks"></a>Comentarios

La interfaz ID3DX10Font se obtiene llamando a [**D3DX10CreateFont**](d3dx10createfont.md) o [**D3DX10CreateFontIndirect.**](d3dx10createfontindirect.md)

El tipo LPD3DX10FONT se define como un puntero a la interfaz ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
