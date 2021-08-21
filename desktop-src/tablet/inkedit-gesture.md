---
description: Se produce cuando se reconoce un gesto de aplicación.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit.Gesture (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a718106f4485682a1b6267f942ec3ef0f5a9fb670449e1f6023d86a5b03af56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032083"
---
# <a name="inkeditgesture-event"></a>InkEdit.Gesture, evento

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

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usó para crear este gesto.

</dd> <dt>

*Trazos* \[ En\]
</dt> <dd>

Colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contiene los [**objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que conste de este gesto.

</dd> <dt>

*Gestos* \[ En\]
</dt> <dd>

Matriz de [**objetos IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) en orden de confianza.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Indica si se debe cancelar la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que conste de este gesto, para no borrar la entrada de lápiz y para que se desenlace [**el evento Stroke.**](inkedit-stroke.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la interfaz IDispatch con un identificador de DISPID \_ IeeGesture.

Solo se genera un evento **Gesture** si [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) para el objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) es el primer objeto **IInkStrokeDisp** desde la última llamada al método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o la última activación del tiempo de espera de reconocimiento.

Si se **cancela el evento Gesture,** se genera el evento [**Stroke**](inkedit-stroke.md) para la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que ha producido el **evento Gesture.**

Para que este evento se produzca, el control [InkEdit](inkedit-control-reference.md) debe suscribirse a un conjunto de gestos de aplicación. Para establecer el interés del control InkEdit en un conjunto de gestos, llame al [**método SetGestureStatus.**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)

Para obtener una lista de los gestos de aplicación, vea el tipo de [**enumeración InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

El [control InkEdit](inkedit-control-reference.md) no reconoce varios gestos de trazo.

El [control InkEdit](inkedit-control-reference.md) se suscribe a los siguientes gestos.



| Gesto                              | Acción               |
|--------------------------------------|----------------------|
| Down-left ,Down-left-long<br/> | Entrar<br/>     |
| Right<br/>                     | Space<br/>     |
| Left<br/>                      | Retroceso<br/> |
| Arriba a la derecha, arriba a la derecha<br/>   | Pestaña<br/>       |



 

Para modificar la acción predeterminada de un gesto:

1.  Agregue controladores de eventos para los eventos **Gesture** [**y Stroke.**](inkedit-stroke.md)
2.  En el controlador de eventos **Gesto,** cancele el **evento Gesto** para el gesto y realice la acción alternativa para el gesto.
3.  En el controlador de eventos [**Stroke,**](inkedit-stroke.md) cancele el evento **Stroke** del [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que ha producido el evento **Gesture** cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkApplicationGesture (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus (método \[ InkEdit) Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Propiedad RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Evento de trazo \[ InkEdit (Control)\]**](inkedit-stroke.md)
</dt> <dt>

[Uso de gestos](using-gestures.md)
</dt> </dl>

 

