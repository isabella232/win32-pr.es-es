---
title: Métodos de ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Métodos de PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681204"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget::P ushAxisAlignedClip métodos)

Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                         | Descripción                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, D2D1 \_ antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes. <br/> |
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , D2D1 \_ antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes. <br/> |



## <a name="remarks"></a>Observaciones

Un par [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) puede aparecer alrededor o dentro de [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), pero no puede superponerse. Por ejemplo, la secuencia de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** es válida, pero la secuencia de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** no es válida.

Este método no devuelve un código de error si se produce un error. Para determinar si una operación de dibujo (como **PushAxisAlignedClip**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [Cómo recortar con un Axis-Aligned rectángulo de recorte](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1 \_ 1. h (incluir D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
