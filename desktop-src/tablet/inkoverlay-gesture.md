---
description: Se produce cuando se reconoce un gesto específico de la aplicación.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay. gesto (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3db800db2d1fca9ee1b00620c698a592ac2121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707152"
---
# <a name="inkoverlaygesture-event"></a>Evento InkOverlay. gesto

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

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento de [**gesto**](inkcollector-gesture.md) .

</dd> <dt>

*Trazos* \[ de\]
</dt> <dd>

La colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como el gesto.

</dd> <dt>

*Gestos* \[ de\]
</dt> <dd>

Matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , en orden de confianza, del reconocedor.

Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Si se debe cancelar la recopilación de este gesto, por ejemplo, no borrar la tinta y activar el evento [**Stroke**](inkcollector-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICEGesture.

Cuando la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre el momento en que un usuario agrega un gesto y el momento en que se produce el evento de [**gesto**](inkcollector-gesture.md) es un valor fijo que no se puede modificar mediante programación. El reconocimiento de gestos es más rápido en el modo **InkAndGesture** .

Para evitar la recopilación de entradas manuscritas en modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Establezca [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) en [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Elimine el trazo en el evento [**Stroke**](inkcollector-stroke.md) .
-   Procesa el gesto en el evento de [**gesto**](inkcollector-gesture.md) .

Para evitar el flujo de tinta mientras se gesturing, establezca la propiedad [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) en **false**.

Además de cuando se inserta la entrada de lápiz, el evento de [**gesto**](inkcollector-gesture.md) se desencadena cuando se está en modo de selección o de borrado. Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.

> [!Note]  
> Para reconocer gestos, debe usar un objeto o un control que pueda recopilar entradas manuscritas.

 

Los gestos de aplicación se definen como gestos que se admiten en la aplicación.

Para que se produzca este evento, el objeto o el control deben tener interés en un conjunto de gestos de la aplicación. Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) del objeto o control.

Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Enumeración InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Usar gestos](using-gestures.md)
</dt> </dl>

 

