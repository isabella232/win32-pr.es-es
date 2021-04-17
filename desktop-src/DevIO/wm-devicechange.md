---
description: Notifica a una aplicación de un cambio en la configuración de hardware de un dispositivo o del equipo.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensaje de WM_DEVICECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423296"
---
# <a name="wm_devicechange-message"></a>Mensaje de DEVICECHANGE de WM \_

Notifica a una aplicación de un cambio en la configuración de hardware de un dispositivo o del equipo.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador **de \_ DEVICECHANGE de WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Evento que se ha producido. Este parámetro puede ser uno de los siguientes valores del archivo de encabezado DBT. h.



| Value                                                                                                                                                                                                                                                                                                  | Significado                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | La configuración actual ha cambiado debido a un acoplamiento o desacoplamiento.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | Se ha producido un evento personalizado.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> </dl>                                         | Se ha insertado un dispositivo o parte de un medio y ahora está disponible.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | Se solicita permiso para quitar un dispositivo o parte de un medio. Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | Se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | Se ha quitado un dispositivo o un medio.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | Se va a quitar un dispositivo o parte de un medio. No se puede denegar.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | Se ha producido un evento específico del dispositivo.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_ DEVNODES \_ cambió](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Se ha agregado o quitado un dispositivo del sistema.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_ USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> </dl>                                                 | El significado de este mensaje está definido por el usuario.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene datos específicos del evento. Su formato depende del valor del parámetro *wParam* . Para obtener más información, consulte la documentación de cada evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para conceder la solicitud.

Devuelve **la \_ consulta \_ de difusión deny** para denegar la solicitud.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos que ofrecen características controlables por software, como la expulsión y el bloqueo, el sistema normalmente envía un mensaje [ \_ DEVICEREMOVEPENDING de DBT](dbt-deviceremovepending.md) para permitir que las aplicaciones y los controladores de dispositivos terminen su uso del dispositivo correctamente. Si el sistema quita de forma forzada un dispositivo, es posible que no envíe un mensaje de [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de hacerlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                                                    |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluye Windows. h o DBT. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

[DBT \_ DEVNODES \_ Changed](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ USERDEFINED](dbt-userdefined.md)
</dt> </dl>

 

