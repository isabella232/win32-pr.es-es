---
description: 'InkCollector.Sysevento temGesture: se produce cuando se reconoce un gesto del sistema.'
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysevento temGesture (Msasisut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f753807d8aaaf03c2de2fd9810ef1e044bcbe05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110062"
---
# <a name="inkcollectorsystemgesture-event"></a>InkCollector.Sysevento temGesture

Se produce cuando se reconoce un gesto del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento SystemGesture.**

</dd> <dt>

*Id.* \[ en\]
</dt> <dd>

Valor del gesto del sistema.

</dd> <dt>

*X* \[ en\]
</dt> <dd>

Coordenada x de la ubicación del gesto.

</dd> <dt>

*Y* \[ en\]
</dt> <dd>

Coordenada Y de la ubicación del gesto.

</dd> <dt>

*Modificador* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*Carácter* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*CursorMode* \[ En\]
</dt> <dd>

Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo borrador. 1 es para el modo normal y 2 para el modo borrador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Los gestos del sistema son útiles porque dan información sobre el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto. También proporcionan accesos directos a combinaciones de eventos del mouse y son formas "más económicas" de detectar eventos del mouse.

Por ejemplo, en lugar de buscar un par de eventos MouseDown Event mousedown de [**mouseup**](inkcollector-mouseup.md)sin que se produzcan otros eventos del mouse entre ellos, puede buscar los gestos del sistema Tap o  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

Como otro ejemplo, en lugar de escuchar eventos [**MouseDown EventMove**](inkcollector-mousedown.md)y obtener numerosos mensajes de  /  [](inkcollector-mousemove.md) **evento MouseMove,** puede ver los [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) gestos del sistema Drag o **RightDrag** siempre que no esté interesado en las coordenadas (x, y) de cada posición del mouse. Esto le permite recibir solo un mensaje en lugar de varios **mensajes mousemove Event.**

Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Para obtener más información sobre los gestos del sistema, vea [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**InkSystemGesture (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Uso de gestos](using-gestures.md)
</dt> <dt>

[Entrada de lápiz, entrada de lápiz y reconocimiento](pen-input--ink--and-recognition.md)
</dt> <dt>

[Entrada de comandos en tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

