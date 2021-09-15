---
description: 'Evento InkPicture.SystemGesture: se produce cuando se reconoce un gesto del sistema.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: Evento InkPicture.SystemGesture (Ms inkut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572332"
---
# <a name="inkpicturesystemgesture-event"></a>Evento InkPicture.SystemGesture

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

Coordenada y de la ubicación del gesto.

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

## <a name="remarks"></a>Observaciones

Los gestos del sistema dan información sobre [**el objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto. También proporcionan accesos directos a combinaciones de eventos del mouse y son formas de detectar eventos del mouse con menos impacto en el rendimiento.

Por ejemplo, en lugar de buscar un par de eventos [**MouseDown Event \[ \]**](inkpicture-mouseup.md) / [**InkPicture Control MouseDown Event \[ InkPicture Control \]**](inkpicture-mousedown.md) sin que se produzcan otros eventos del mouse entre ellos, puede buscar los gestos del sistema Tap o RightTap.

Como otro ejemplo, en lugar de escuchar los eventos [**\[ MousePicture \] Control MouseMove**](inkpicture-mousedown.md)Event InkPicture Control / [**\[ \]**](inkpicture-mousemove.md) y obtener numerosos mensajes del **control \[ \] MouseMove Event InkPicture,** puede observar los gestos del sistema Drag o RightDrag siempre que no esté interesado en las coordenadas (x, y) de cada posición del mouse. Esto le permite recibir solo un mensaje en lugar de varios mensajes **mousemove Event \[ InkPicture Control. \]**

Para obtener una lista de gestos del sistema específicos, vea el tipo [**de enumeración InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Para obtener más información sobre los gestos del sistema, vea [Usar gestos](using-gestures.md) y [entradas de comandos en tablet PC.](/previous-versions//dd314533(v=vs.85))

Este método de evento se define en las interfaces de solo envío (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkSystemGesture (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Uso de gestos](using-gestures.md)
</dt> </dl>

 

