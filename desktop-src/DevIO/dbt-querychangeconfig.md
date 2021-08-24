---
description: El sistema difunde el evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual \_ (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e9c222fdc29f635263b45b5fd7e54ee229a33d7dee1ff31cd1e3072bfe6e84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318425"
---
# <a name="dbt_querychangeconfig-event"></a>Evento DBT \_ QUERYCHANGECONFIG

El sistema difunde el evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual \_ (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ DEVICECHANGE**](wm-devicechange.md) de WM con *wParam* establecido en DBT \_ QUERYCHANGECONFIG y *lParam* establecido en cero.


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

Identificador [**del mensaje \_ DEVICECHANGE**](wm-devicechange.md) de WM.

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
| Header<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Administración de dispositivos eventos](device-management-events.md)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




