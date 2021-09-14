---
description: El sistema envía el evento de dispositivo \_ DBT CUSTOMEVENT cuando se ha producido un evento personalizado definido por el controlador.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164481"
---
# <a name="dbt_customevent-event"></a>Evento \_ CUSTOMEVENT de DBT

El sistema envía el evento de dispositivo \_ DBT CUSTOMEVENT cuando se ha producido un evento personalizado definido por el controlador.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ WM DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT CUSTOMEVENT y lParam establecidos como se describe a \_ continuación. 


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

Establezca en DBT \_ CUSTOMEVENT.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) de DEV y, a continuación, compruebe su **miembro \_ dbch devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

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

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




