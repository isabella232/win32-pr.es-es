---
title: Métodos DrawText de ID2D1RenderTarget
description: Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Métodos DrawText de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 430607b09795be249a05398b1bfb749e9be45ae517c6374e001a4c3042bf316f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874195"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>Métodos ID2D1RenderTarget::D rawText

Dibuja el texto especificado utilizando la información de formato proporcionada por un [**objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                                                                               | Descripción                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText(WCHAR \* ,IDWriteTextFormat \* ,D2D1 \_ RECT \_ F&,ID2D1Brush \* ,D2D1 \_ DRAW \_ TEXT \_ OPTIONS,DWRITE \_ TEXT \_ MEASURING \_ METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Dibuja el texto especificado utilizando la información de formato proporcionada por un [**objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)<br/>  |
| [**DrawText(WCHAR \* ,IDWriteTextFormat \* ,D2D1 \_ RECT \_ F \* ,ID2D1Brush \* ,D2D1 \_ DRAW \_ TEXT \_ OPTIONS,DWRITE \_ TEXT \_ MEASURING \_ METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Dibuja el texto especificado utilizando la información de formato proporcionada por un [**objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) <br/> |



## <a name="remarks"></a>Comentarios

Para dibujar texto con Direct2D, use el método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para el texto que tiene un único formato o el método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) cuando necesite varios formatos, características avanzadas de OpenType o pruebas de llamadas. Estos métodos usan la API DirectWrite para proporcionar una presentación de texto de alta calidad.

Este método no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **DrawText),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [vea Cómo dibujar texto](how-to--draw-text.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Dibujar texto](how-to--draw-text.md)
</dt> <dt>

[Información general sobre formato y diseño de texto](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

