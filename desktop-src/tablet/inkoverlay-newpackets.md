---
description: Se produce cuando el recopiladores de entrada de lápiz resocia un paquete.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Evento InkOverlay.NewPackets (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2571e7c8f97881da5bbbef6cdab093ce2d3107b5482def5b62d2dfa141c7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219209"
---
# <a name="inkoverlaynewpackets-event"></a>Evento InkOverlay.NewPackets

Se produce cuando el recopiladores de entrada de lápiz resocia un paquete.

## <a name="syntax"></a>Sintaxis


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento NewInAirPackets.**](inkcollector-newinairpackets.md)

</dd> <dt>

*Trazo* \[ En\]
</dt> <dd>

Especifica el [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketCount* \[ En\]
</dt> <dd>

Número de paquetes recibidos para un [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Matriz que contiene los datos seleccionados para el paquete.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Los paquetes se reciben mientras se recopila un trazo. Los eventos de paquetes se producen rápidamente y un controlador de eventos [**NewPackets**](inkcollector-newpackets.md) debe ser rápido o el rendimiento se vería afectado.

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICENewPackets.

Este evento debe usarse cuidadosamente, ya que podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.

Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto del recopilador de lápiz. La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.

> [!Note]  
> Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Evento NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




