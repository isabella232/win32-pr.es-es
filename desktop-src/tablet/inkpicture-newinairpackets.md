---
description: 'Evento InkPicture.NewInAirPackets: se produce cuando se ve un paquete en el aire.'
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Evento InkPicture.NewInAirPackets (Msasisut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f81f6f485329eaa5cd96c2aece39646e700a21bc762c5d66344e5daf0a628f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967054"
---
# <a name="inkpicturenewinairpackets-event"></a>Evento InkPicture.NewInAirPackets

Se produce cuando se ve un paquete en el aire.

## <a name="syntax"></a>Sintaxis


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento NewInAirPackets.**

</dd> <dt>

*PacketCount* \[ En\]
</dt> <dd>

Número de paquetes en aire recibidos.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Matriz que contiene los datos seleccionados para el paquete.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Se crea un paquete en el aire cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto del recopilador de entrada de lápiz o el usuario mueve un mouse dentro de la ventana asociada del objeto del recopilador de lápiz. **Los eventos NewInAirPackets** se generan rápidamente y el controlador de eventos debe ser rápido o el rendimiento sufra.

Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ de IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICENewInAirPackets.

El **evento NewInAirPackets** se desencadena incluso cuando está en modo de selección o borrado, no solo al insertar entrada de lápiz. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) del objeto de recopilador de lápiz. La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.

> [!Note]  
> Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[**Evento NewPackets**](inkpicture-newpackets.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




