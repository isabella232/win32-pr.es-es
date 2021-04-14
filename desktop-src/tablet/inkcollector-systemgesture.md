---
description: Se produce cuando se reconoce un gesto del sistema.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541286"
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

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **SystemGesture** .

</dd> <dt>

*ID.* \[ en\]
</dt> <dd>

Valor del gesto del sistema.

</dd> <dt>

*X* \[ en\]
</dt> <dd>

Coordenada x de la ubicación del gesto.

</dd> <dt>

*Y* \[ en\]
</dt> <dd>

Coordenada y de la ubicación del gesto.

</dd> <dt>

*Modificador* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*Carácter* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*CursorMode* \[ de\]
</dt> <dd>

Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo de borrador. 1 es para el modo normal y 2 para el modo de borrador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los gestos del sistema son útiles porque proporcionan información sobre el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto. También proporcionan accesos directos a combinaciones de eventos del mouse y son formas "más baratas" de detectar eventos del mouse.

Por ejemplo, en lugar de buscar un par de eventos MouseDown del [**evento MouseUp**](inkcollector-mouseup.md)  /  [](inkcollector-mousedown.md) de eventos sin que se produzcan otros eventos del mouse en, puede buscar los gestos del sistema [**TAP**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightTap** .

Otro ejemplo, en lugar de realizar escuchas de eventos de evento de evento de evento [**MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) y obtener numerosos mensajes de **eventos de MouseMove** , puede ver los gestos de [**arrastrar**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag** del sistema siempre que no le interesen las coordenadas (x, y) de cada posición del mouse. Esto le permite recibir solo un mensaje en lugar de numerosos mensajes de **eventos de MouseMove** .

Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Para obtener más información acerca de los gestos del sistema, consulte [uso de gestos](using-gestures.md) y [entradas de comandos en Tablet PC](/previous-versions//dd314533(v=vs.85)).

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**Enumeración InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Usar gestos](using-gestures.md)
</dt> <dt>

[Entrada de lápiz, tinta y reconocimiento](pen-input--ink--and-recognition.md)
</dt> <dt>

[Entrada de comando en Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

