---
description: Se envía cuando VMR ha seleccionado su mecanismo de representación.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680468"
---
# <a name="ec_vmr_renderdevice_set"></a>EC \_ VMR \_ RENDERDEVICE \_ set

Se envía cuando VMR ha seleccionado su mecanismo de representación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Puede ser uno de los siguientes valores:



| Value                        | Significado                                                  |
|------------------------------|----------------------------------------------------------|
| superposición de dispositivo de representación de VMR \_ \_ \_ | La VMR se representará en la superficie de superposición (solo VMR-7). |
| \_VIDMEM de \_ dispositivo de representación VMR \_  | La VMR se representará en la memoria de vídeo.                     |
| \_SYSMEM de \_ dispositivo de representación VMR \_  | La VMR se representará en la memoria del sistema (solo VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento lo envían los eventos VMR-7 y VMR-9 y se reenvían a las aplicaciones. Tenga en cuenta que VMR-9 solo admite destinos de representación de memoria de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




