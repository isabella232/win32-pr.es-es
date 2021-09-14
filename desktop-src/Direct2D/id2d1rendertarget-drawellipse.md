---
title: Métodos de ID2D1RenderTarget DrawVelopse (D2d1.h)
description: Dibuja el contorno de una elipse con las dimensiones y el trazo especificados.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Métodos DrawVelopse de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162813"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>Métodos ID2D1RenderTarget::D rawRenderpse

Dibuja el contorno de una elipse con las dimensiones y el trazo especificados.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                 | Descripción                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawVelopse(D2D1 \_ ELLIPSE&,ID2D1Brush \* ,FLOAT,ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | Dibuja el contorno de la elipse especificada utilizando el estilo de trazo especificado. <br/> |
| [**DrawVelopse(D2D1 \_ ELLIPSE \* ,ID2D1Brush \* ,FLOAT,ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | Dibuja el contorno de la elipse especificada utilizando el estilo de trazo especificado. <br/> |



## <a name="remarks"></a>Observaciones

El **método DrawVelopse** no devuelve un código de error si se produce un error. Para determinar si se ha producido un error en una operación de dibujo (como **DrawVelopse),** compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [vea Cómo dibujar y rellenar una forma básica.](how-to-draw-an-ellipse.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**FillVelopse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
