---
title: Métodos ID2D1RenderTarget FillVelopse (D2d1.h)
description: Pinta el interior de la elipse especificada.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Métodos de FillVelopse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7ee6624e5f557bb82924b4fa0f77d88a9cec35775a72009608120e8b8f2bd063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874175"
---
# <a name="id2d1rendertargetfillellipse-methods"></a>Métodos ID2D1RenderTarget::FillVelopse

Pinta el interior de la elipse especificada.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                             | Descripción                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| [**FillVelopse(D2D1 \_ ELLIPSE&,ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))  | Pinta el interior de la elipse especificada. <br/> |
| [**FillVelopse(D2D1 \_ ELLIPSE \* ,ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) | Pinta el interior de la elipse especificada. <br/> |



## <a name="remarks"></a>Comentarios

Este método no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **FillVelopse),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [vea Cómo dibujar y rellenar una forma básica.](how-to-draw-an-ellipse.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Dibujar y rellenar una forma básica](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
