---
description: El sistema difunde el evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual \_ (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164445"
---
# <a name="dbt_querychangeconfig-event"></a>Evento \_ DBT QUERYCHANGECONFIG

El sistema difunde el evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual \_ (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ WM DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT \_ QUERYCHANGECONFIG y *lParam* establecido en cero.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador [**del mensaje WM \_ DEVICECHANGE.**](wm-devicechange.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Establezca en DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Establecer en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para conceder permiso para cambiar la configuración.

Devuelve BROADCAST \_ QUERY DENY para denegar el permiso para cambiar la \_ configuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Administración de dispositivos eventos](device-management-events.md)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




