---
title: Métodos ID2D1RenderTarget CreateBitmapBrush
description: Crea un objeto ID2D1BitmapBrush a partir del mapa de bits especificado.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Métodos CreateBitmapBrush de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 411ae2dd81fce88bec5d6a3717fe79d942de84f060c53a90b83cae461d6a49de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053095"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Métodos ID2D1RenderTarget::CreateBitmapBrush

Crea un [**objeto ID2D1BitmapBrush a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) del mapa de bits especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush(ID2D1Bitmap \* ,D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Crea un [**objeto ID2D1BitmapBrush a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) del mapa de bits especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Crea un [**objeto ID2D1BitmapBrush a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) del mapa de bits especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Crea un [**objeto ID2D1BitmapBrush a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) del mapa de bits especificado. El pincel usa los valores predeterminados para su modo de extensión, modo de interpolación, opacidad y transformación.<br/> |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Crea un [**objeto ID2D1BitmapBrush a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) del mapa de bits especificado. El pincel usa los valores predeterminados para su opacidad y transformación.<br/>                                   |



## <a name="examples"></a>Ejemplos

Para obtener un ejemplo en el que se muestra cómo pintar un área con un pincel de mapa de bits, [vea How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Cómo crear un pincel de mapa de bits](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> </dl>

 

