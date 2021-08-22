---
description: Se envía cuando vmr ha seleccionado su mecanismo de representación.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2c8bef78156c4438e1e4e7aea45326562002ed8f4a3786377d7ee43a00a57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015863"
---
# <a name="ec_vmr_renderdevice_set"></a>EC \_ VMR \_ RENDERDEVICE \_ SET

Se envía cuando vmr ha seleccionado su mecanismo de representación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Puede ser uno de los siguientes valores:



| Valor                        | Significado                                                  |
|------------------------------|----------------------------------------------------------|
| SUPERPOSICIÓN DEL DISPOSITIVO \_ DE REPRESENTACIÓN \_ DE VMR \_ | La VMR se representará en la superficie superpuesta (solo VMR-7). |
| VMR \_ RENDER \_ DEVICE \_ VIDMEM  | VmR se representará en la memoria de vídeo.                     |
| VMR \_ RENDER \_ DEVICE \_ SYSMEM  | La VMR se representará en la memoria del sistema (solo VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

VmR-7 y VMR-9 envían este evento y se reenvía a las aplicaciones. Tenga en cuenta que VMR-9 solo admite destinos de representación de memoria de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




