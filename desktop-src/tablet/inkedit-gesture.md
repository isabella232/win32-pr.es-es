---
description: Se produce cuando se reconoce un gesto de aplicación.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. gesto (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277400"
---
# <a name="inkeditgesture-event"></a>Evento InkEdit. gesto

Se produce cuando se reconoce un gesto de aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usó para crear este gesto.

</dd> <dt>

*Trazos* \[ de\]
</dt> <dd>

La colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contiene los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que componen este gesto.

</dd> <dt>

*Gestos* \[ de\]
</dt> <dd>

Una matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , en orden de confianza.

Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Indica si se debe cancelar la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que constituye este gesto, de modo que no se borre la tinta y se desencadene el evento [**Stroke**](inkedit-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de DISPID \_ IeeGesture.

Un evento de **gesto** solo se desencadena si el [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) del objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) es el primer objeto **IInkStrokeDisp** desde la última llamada al método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o la última activación del tiempo de espera del reconocimiento.

Si se cancela el evento de **gesto** , se genera el evento de [**trazo**](inkedit-stroke.md) para la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que provocó el evento de **gesto** .

Para que se produzca este evento, el control [InkEdit](inkedit-control-reference.md) debe suscribirse a un conjunto de gestos de aplicación. Para establecer el interés del control InkEdit en un conjunto de gestos, llame al método [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .

Para obtener una lista de los gestos de aplicación, vea el tipo de enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

El control [InkEdit](inkedit-control-reference.md) no reconoce varios gestos de trazo.

El control [InkEdit](inkedit-control-reference.md) se suscribe a los siguientes movimientos.



| Gesto                              | Acción               |
|--------------------------------------|----------------------|
| Abajo-izquierda, hacia abajo y a la izquierda<br/> | Entrar<br/>     |
| Right<br/>                     | Space<br/>     |
| Left<br/>                      | Retroceso<br/> |
| Arriba a la derecha, arriba y a la derecha<br/>   | Pestaña<br/>       |



 

Para modificar la acción predeterminada de un gesto:

1.  Agregue controladores de eventos para los eventos de **gestos** y [**trazos**](inkedit-stroke.md) .
2.  En el controlador de eventos de **gestos** , cancele el evento de **gesto** para el gesto y realice la acción alternativa para el gesto.
3.  En el controlador de eventos [**Stroke**](inkedit-stroke.md) , cancele el evento **Stroke** para el objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que ha generado el evento de **gesto** cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeración InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Control InkEdit del método SetGestureStatus \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Propiedad RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Control InkEdit de evento Stroke \[\]**](inkedit-stroke.md)
</dt> <dt>

[Usar gestos](using-gestures.md)
</dt> </dl>

 

