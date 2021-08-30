---
title: Métodos de DrawBitmap id2D1RenderTarget
description: Dibuja el id2D1Bitmap especificado.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Métodos DrawBitmap de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 46c4e163ebb7c5c17db743687fded2c0f32771a37c0fb4dfa8af9ce45ee2fb86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874355"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>Métodos ID2D1RenderTarget::D rawBitmap

Dibuja el [**id2D1Bitmap especificado.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                       | Descripción                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**DrawBitmap(ID2D1Bitmap \* , D2D1 \_ RECT F \_&,FLOAT,D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE,D2D1 \_ RECT F \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | Dibuja el mapa de bits especificado después de escalarlo al tamaño del rectángulo especificado. <br/> |
| [**DrawBitmap(ID2D1Bitmap \* , D2D1 \_ RECT F \_&,FLOAT,D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE,D2D1 \_ RECT F \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | Dibuja el mapa de bits especificado después de escalarlo al tamaño del rectángulo especificado. <br/> |
| [**DrawBitmap(ID2D1Bitmap, \* D2D1 \_ RECT \_ F , \* FLOAT,D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE,D2D1 \_ RECT F \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | Dibuja el mapa de bits especificado después de escalarlo al tamaño del rectángulo especificado. <br/> |



## <a name="remarks"></a>Comentarios

Este método no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **DrawBitmap),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [vea Cómo dibujar un mapa de bits.](how-to-draw-a-bitmap.md) Para obtener un ejemplo en el que se muestra cómo cargar un mapa de bits desde un recurso o un [archivo,](how-to-load-a-direct2d-bitmap-from-a-file.md)vea Cómo cargar un mapa de [bits](how-to-load-a-bitmap-from-a-resource.md) desde un recurso y Cómo cargar un mapa de bits desde un archivo .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Dibujar un mapa de bits](how-to-draw-a-bitmap.md)
</dt> <dt>

[Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[Cómo cargar un mapa de bits desde un archivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

