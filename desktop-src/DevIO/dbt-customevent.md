---
description: El sistema envía el evento de dispositivo DBT CUSTOMEVENT cuando se ha producido \_ un evento personalizado definido por el controlador.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75ec02262e4cf49a7b929f738acce94822aaf67a397a37d6237f4faa57ef7f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109045"
---
# <a name="dbt_customevent-event"></a>Evento \_ CUSTOMEVENT de DBT

El sistema envía el evento de dispositivo DBT CUSTOMEVENT cuando se ha producido \_ un evento personalizado definido por el controlador.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ DEVICECHANGE**](wm-devicechange.md) de WM con *wParam* establecido en DBT CUSTOMEVENT y lParam establecido como se \_ describe a continuación. 


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

Se establece en DBT \_ CUSTOMEVENT.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ \_ DEV BROADCAST HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

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

 

 




