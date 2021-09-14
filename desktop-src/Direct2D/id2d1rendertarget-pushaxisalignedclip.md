---
title: Métodos ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1.h)
description: Especifica un rectángulo al que se recortan todas las operaciones de dibujo posteriores.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Métodos PushAxisAlignedClip de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162777"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>Métodos ID2D1RenderTarget::P ushAxisAlignedClip

Especifica un rectángulo al que se recortan todas las operaciones de dibujo posteriores.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                         | Descripción                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F&,D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Especifica un rectángulo al que se recortan todas las operaciones de dibujo posteriores. <br/> |
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F , \* D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Especifica un rectángulo al que se recortan todas las operaciones de dibujo posteriores. <br/> |



## <a name="remarks"></a>Observaciones

Un [**par PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) puede producirse alrededor o dentro de [**pushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)pero no se pueden superponer. Por ejemplo, la secuencia de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** es válida, pero la secuencia de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip** y **PopLayer** no es válida.

Este método no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **PushAxisAlignedClip),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1 \_ 1.h (incluir D2d1.h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
