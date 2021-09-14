---
description: Se quitó Plug and Play dispositivo o volvió a estar disponible.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061190"
---
# <a name="ec_device_lost"></a>DISPOSITIVO EC \_ \_ PERDIDO

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

## <a name="remarks"></a>Observaciones

Cuando el dispositivo vuelve a estar disponible, el estado anterior del filtro del dispositivo ya no es válido. La aplicación debe recompilar el gráfico para poder usar el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Notificación de eliminación de dispositivos](device-removal-notification.md)
</dt> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




