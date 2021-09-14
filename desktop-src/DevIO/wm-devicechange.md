---
description: Notifica a una aplicación un cambio en la configuración de hardware de un dispositivo o del equipo.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensaje WM_DEVICECHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164278"
---
# <a name="wm_devicechange-message"></a>Mensaje \_ DE WM DEVICECHANGE

Notifica a una aplicación un cambio en la configuración de hardware de un dispositivo o del equipo.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador **DE WM \_ DEVICECHANGE.**

</dd> <dt>

*wParam* 
</dt> <dd>

Evento que se ha producido. Este parámetro puede ser uno de los siguientes valores del archivo de encabezado Dbt.h.

| Value | Significado |
|-------|---------|
| **[DBT \_ DEVNODES \_ CHANGED](dbt-devnodes-changed.md)**</br>0x0007 | Se ha agregado o quitado un dispositivo del sistema. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar). |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | La configuración actual ha cambiado, debido a un acoplamiento o desacoplado. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar). |
| **[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</br>0x8000 | Se ha insertado un dispositivo o un elemento multimedia y ahora está disponible. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | Se solicita permiso para quitar un dispositivo o un elemento multimedia. Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Un dispositivo o un elemento multimedia está a punto de quitarse. No se puede denegar. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Se ha quitado un dispositivo o un elemento multimedia. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Se ha producido un evento específico del dispositivo. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Se ha producido un evento personalizado. |
| **[DBT \_ DEFINIDO POR EL USUARIO](dbt-userdefined.md)**</br>0xFFFF | El significado de este mensaje está definido por el usuario. |

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene datos específicos del evento. Su formato depende del valor del *parámetro wParam.* Para más información, consulte la documentación de cada evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para conceder la solicitud.

Devuelve **BROADCAST QUERY DENY \_ \_ para** denegar la solicitud.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos que ofrecen características controlables por software, como la expulsión y el bloqueo, el sistema normalmente envía un mensaje [ \_ DBT DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que las aplicaciones y los controladores de dispositivos finalicen correctamente el uso del dispositivo. Si el sistema quita forzadamente un dispositivo, es posible que no envíe un mensaje [ \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) de DBT antes de hacerlo.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows XP |
| Servidor mínimo compatible | Windows Server 2003|
| Encabezado | <dl> <dt>Winuser.h (incluya Windows.h o Dbt.h)</dt> </dl> |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ CHANGED](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ DEFINIDO POR EL USUARIO](dbt-userdefined.md)
</dt> </dl>
