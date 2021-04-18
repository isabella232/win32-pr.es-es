---
description: Se produce cuando el recopilador de tinta recibe un paquete.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0b3e1df0df2ba051150550daa60772e2a068df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716305"
---
# <a name="inkpicturenewpackets-event"></a>Evento InkPicture. NewPackets

Se produce cuando el recopilador de tinta recibe un paquete.

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

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**NewInAirPackets**](inkpicture-newinairpackets.md) .

</dd> <dt>

*Trazo* \[ de de\]
</dt> <dd>

El objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketCount* \[ de\]
</dt> <dd>

El número de paquetes recibidos para un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Una matriz que contiene los datos seleccionados para el paquete.

Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los paquetes se reciben mientras se recopila un trazo. Los eventos de paquetes se producen rápidamente y un controlador de eventos **NewPackets** debe ser rápido o se ve afectado por el rendimiento.

Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICENewPackets.

Este evento debe usarse con cuidado, ya que podría tener un efecto adverso en el rendimiento de la tinta si se ejecuta demasiado código en los controladores de eventos.

Para establecer qué propiedades están contenidas en esta matriz, use la propiedad [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de tinta. La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.

> [!Note]  
> Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento NewInAirPackets**](inkpicture-newinairpackets.md)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




