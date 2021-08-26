---
description: Se quitó Plug and Play dispositivo o volvió a estar disponible.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4868890967d6448226c1f000ab06b7ccbcf7a06e3062d1cdef03e0ad960bc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998165"
---
# <a name="ec_device_lost"></a>DISPOSITIVO \_ EC \_ PERDIDO

Se quitó Plug and Play dispositivo o volvió a estar disponible.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntero a la **interfaz IUnknown** del filtro que representa el dispositivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero si se quitó el dispositivo o 1 si el dispositivo está disponible de nuevo.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Cuando el dispositivo vuelve a estar disponible, el estado anterior del filtro del dispositivo ya no es válido. La aplicación debe volver a generar el gráfico para poder usar el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Notificación de eliminación de dispositivos](device-removal-notification.md)
</dt> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




