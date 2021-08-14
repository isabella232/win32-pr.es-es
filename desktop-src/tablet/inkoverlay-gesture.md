---
description: 'Evento InkOverlay.Gesture: se produce cuando se reconoce un gesto específico de la aplicación.'
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay.Gesture (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01689465e9951a5b8cd6548cabb0be4a0bde32c7cf46c2ea4c71b3bb38151eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219316"
---
# <a name="inkoverlaygesture-event"></a>Evento InkOverlay.Gesture

Se produce cuando se reconoce un gesto específico de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
void Gesture(
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

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento Gesture.**](inkcollector-gesture.md)

</dd> <dt>

*Trazos* \[ En\]
</dt> <dd>

Colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como gesto.

</dd> <dt>

*Gestos* \[ En\]
</dt> <dd>

Matriz de [**objetos IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) en orden de confianza, del reconocedor.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Si se debe cancelar la colección de este gesto, por ejemplo, no borrar la entrada de lápiz y se debe abrir el [**evento Stroke.**](inkcollector-stroke.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents con un identificador DE \_ DISPID ICEGesture.

Cuando la [**propiedad CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre cuando un usuario agrega un gesto y cuando se produce el evento [**Gesture**](inkcollector-gesture.md) es un valor fijo que no se puede modificar mediante programación. El reconocimiento de gestos es más **rápido en el modo InkAndGesture.**

Para evitar la recopilación de lápiz en [**el modo InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Establezca [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) en [**InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Elimine el trazo en el [**evento Stroke.**](inkcollector-stroke.md)
-   Procese el gesto en el [**evento Gesto.**](inkcollector-gesture.md)

Para evitar el flujo de entrada de lápiz mientras se gesura, establezca [**la propiedad DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) en **FALSE.**

Además de al insertar la entrada de lápiz, el [**evento Gesto**](inkcollector-gesture.md) se desencadena cuando está en modo de selección o borrado. Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.

> [!Note]  
> Para reconocer gestos, debe usar un objeto o control que pueda recopilar lápiz.

 

Los gestos de aplicación se definen como gestos que se admiten dentro de la aplicación.

Para que se produzca este evento, el objeto o control debe tener interés en un conjunto de gestos de aplicación. Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al [**método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) del objeto o control.

Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**InkApplicationGesture (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Uso de gestos](using-gestures.md)
</dt> </dl>

 

