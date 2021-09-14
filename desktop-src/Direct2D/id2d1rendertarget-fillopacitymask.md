---
title: Métodos ID2D1RenderTarget FillOpacityMask
description: Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Métodos fillOpacityMask de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162798"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>Métodos ID2D1RenderTarget::FillOpacityMask

Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                          | Descripción                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FillOpacityMask(ID2D1Bitmap \* ,ID2D1Brush \* ,D2D1 \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT F \_&,D2D \_ RECT F \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación. <br/> |
| [**FillOpacityMask(ID2D1Bitmap \* ,ID2D1Brush \* ,D2D1 \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT F \_ \* ,D2D \_ RECT F \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación. <br/> |



## <a name="remarks"></a>Observaciones

Para que este método funcione correctamente, el destino de representación debe usar el modo de suavizado de contorno [**D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) Puede establecer el modo de suavizado de contorno llamando al [**método ID2D1RenderTarget::SetAntialiasMode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode)

Este método no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **FillOpacityMask),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

