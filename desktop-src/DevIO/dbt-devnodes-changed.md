---
description: El sistema difunde el evento de dispositivo \_ DBT DEVNODES CHANGED cuando se ha agregado o quitado un dispositivo \_ del sistema. Las aplicaciones que mantienen listas de dispositivos en el sistema deben actualizar sus listas.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d43873241c3f72336dd996fb9fa3486229d9ffcf522923d68ab606313afb7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539165"
---
# <a name="dbt_devnodes_changed-event"></a>Evento \_ DBT DEVNODES \_ CHANGED

El sistema difunde el evento de dispositivo \_ DBT DEVNODES CHANGED cuando se ha agregado o quitado un dispositivo \_ del sistema. Las aplicaciones que mantienen listas de dispositivos en el sistema deben actualizar sus listas.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ DEVICECHANGE**](wm-devicechange.md) de WM con *wParam* establecido en DBT \_ DEVNODES CHANGED y \_ *lParam* establecido en cero.


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

Se establece en DBT \_ DEVNODES \_ CHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Establecer en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

No hay información adicional sobre qué dispositivo se ha agregado o quitado del sistema. Las aplicaciones que requieren más información deben registrarse para la notificación del dispositivo mediante [**la función RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Administración de dispositivos eventos](device-management-events.md)
</dt> <dt>

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




