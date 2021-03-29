---
title: ID2D1RenderTarget métodos DrawText
description: Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Métodos DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679221"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget::D rawText métodos)

Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                                                                               | Descripción                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ Options, DWRITE \_ Text \_ mediing \_ Method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .<br/>  |
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ Options, DWRITE \_ Text \_ mediing \_ Method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) . <br/> |



## <a name="remarks"></a>Observaciones

Para dibujar texto con Direct2D, use el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para el texto que tiene un formato único, o el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) cuando necesite varios formatos, características OpenType avanzadas o pruebas de posicionamiento. Estos métodos usan la API de DirectWrite para proporcionar una presentación de texto de alta calidad.

Este método no devuelve un código de error si se produce un error. Para determinar si una operación de dibujo (como **DrawText**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Cómo dibujar texto](how-to--draw-text.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Cómo dibujar texto](how-to--draw-text.md)
</dt> <dt>

[Información general sobre el diseño y el formato de texto](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

