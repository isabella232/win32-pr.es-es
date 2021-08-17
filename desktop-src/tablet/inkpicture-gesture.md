---
description: 'Evento InkPicture.Gesture: se produce cuando se reconoce un gesto específico de la aplicación.'
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture.Gesture (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c0307397fc5a197666894d40adce6f4a579e22d896df8df645b053580ee94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451074"
---
# <a name="inkpicturegesture-event"></a>Evento InkPicture.Gesture

Se produce cuando se reconoce un *gesto específico de* la aplicación.

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

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Gesture.**

</dd> <dt>

*Trazos* \[ En\]
</dt> <dd>

Colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como gesto.

</dd> <dt>

*Gestos* \[ En\]
</dt> <dd>

Matriz de [**objetos IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) en orden de confianza, del reconocedor.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** si se debe cancelar este evento, por ejemplo, para no borrar la entrada manuscrita y para que se desprenda el [**evento Stroke.**](inkpicture-stroke.md) De lo contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío (dispinterfaces) **\_ de IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE \_ DISPID ICEGesture.

Cuando la [**propiedad CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre cuando un usuario agrega un gesto y cuando se produce el evento **Gesture** es un valor fijo que no se puede modificar mediante programación. El reconocimiento de gestos es más **rápido en el modo InkAndGesture.**

Para evitar la recopilación de entrada de lápiz en [**el modo InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Establezca [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) en [**InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Elimine el trazo en el [**evento Stroke.**](inkpicture-stroke.md)
-   Procese el gesto en el **evento Gesto.**

Para evitar el flujo de entrada de lápiz durante la gesuración, establezca [**la propiedad DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) en **FALSE.**

Además de al insertar la entrada de lápiz, el **evento Gesto** se desencadena cuando está en modo de selección o borrado. Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.

> [!Note]  
> Para reconocer gestos, debe usar un objeto o control que pueda recopilar entrada manuscrita.

 

Los gestos de aplicación se definen como gestos que se admiten dentro de la aplicación.

Para que se produzca este evento, el objeto o control debe tener interés en un conjunto de gestos de aplicación. Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al [**método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) del objeto o control.

Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkApplicationGesture (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[Uso de gestos](using-gestures.md)
</dt> </dl>

 

