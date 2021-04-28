---
description: 'Evento InkCollector.NewPackets: se produce cuando el recopilador de entrada de lápiz recibe un paquete.'
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector.NewPackets (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110123"
---
# <a name="inkcollectornewpackets-event"></a>Evento InkCollector.NewPackets

Se produce cuando el recopilador de entrada de lápiz recibe un paquete.

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

Cuando este método vuelve, contiene una matriz que contiene los datos seleccionados para el paquete.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Los paquetes se reciben mientras se recopila un trazo. Los eventos de paquetes se producen rápidamente y un controlador de eventos **NewPackets** debe ser rápido o el rendimiento se vería afectado.

El método de evento TThis se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents con un identificador de DISPID \_ ICENewPackets.

Este evento debe usarse cuidadosamente, ya que podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.

Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto del recopilador de entrada de lápiz. La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.

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

[**Evento NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




