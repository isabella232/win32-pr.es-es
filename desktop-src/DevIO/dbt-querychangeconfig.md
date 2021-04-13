---
description: El sistema difunde el \_ evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Evento DBT_QUERYCHANGECONFIG (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538890"
---
# <a name="dbt_querychangeconfig-event"></a>\_Evento DBT QUERYCHANGECONFIG

El sistema difunde el \_ evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.

Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ QUERYCHANGECONFIG y *lParam* establecido en cero.


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

*identificador* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Establézcalo en DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Establecer en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para conceder permiso para cambiar la configuración.

Devuelve \_ la consulta \_ de difusión deny para denegar el permiso para cambiar la configuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Eventos de administración de dispositivos](device-management-events.md)
</dt> <dt>

[**DEVICECHANGE de WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




