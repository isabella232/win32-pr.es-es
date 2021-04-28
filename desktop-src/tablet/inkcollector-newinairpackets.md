---
description: 'Evento InkCollector.NewInAirPackets: se produce cuando se ve un paquete en el aire.'
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: Evento InkCollector.NewInAirPackets (Msiguaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5709ae0b468aa6ab49516accf4037695268788
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110133"
---
# <a name="inkcollectornewinairpackets-event"></a>Evento InkCollector.NewInAirPackets

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

Cuando este método devuelve un resultado, contiene una matriz que contiene los datos seleccionados para el paquete.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Se crea un paquete en el aire cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto del recopilador de entrada de lápiz o el usuario mueve un mouse dentro de la ventana asociada del objeto del recopilador de lápiz. **Los eventos NewInAirPackets** se generan rápidamente y el controlador de eventos debe ser rápido o el rendimiento sufra.

Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE \_ DISPID ICENewInAirPackets.

El **evento NewInAirPackets** se desencadena incluso cuando está en modo de selección o borrado, no solo al insertar entrada de lápiz. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de lápiz. La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.

> [!Note]  
> Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.

 

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

[**Propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Evento NewPackets**](inkcollector-newpackets.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




