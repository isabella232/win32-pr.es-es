---
description: La interfaz ID3DXFont encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interfaz ID3DXFont (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060596"
---
# <a name="id3dxfont-interface"></a>Interfaz ID3DXFont

La interfaz ID3DXFont encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.

## <a name="members"></a>Members

La **interfaz ID3DXFont** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFont** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXFont** tiene estos métodos.



| Método                                                    | Descripción                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dxfont--drawtext.md)                   | Dibuja texto con formato. Este método admite cadenas ANSI y Unicode.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Devuelve un identificador a un contexto de dispositivo de presentación (DC) que tiene el conjunto de fuentes.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ DESCA,** respectivamente.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Recupera el dispositivo Direct3D asociado al objeto de fuente.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Recupera las características de fuente que se identifican en una [**estructura TEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) Este método admite la configuración del compilador ANSI y Unicode.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo. Este método admite cadenas ANSI y Unicode.<br/>                                                                                        |



 

## <a name="remarks"></a>Observaciones

La **interfaz ID3DXFont** se obtiene mediante una llamada a [**D3DXCreateFont**](d3dxcreatefont.md) o [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).

El tipo LPD3DXFONT se define como un puntero a la **interfaz ID3DXFont.**


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
