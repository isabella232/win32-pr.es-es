---
description: El sistema difunde el evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo \_ o un elemento multimedia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: DBT_DEVICEQUERYREMOVE evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164477"
---
# <a name="dbt_devicequeryremove-event"></a>Evento \_ DEVICEQUERYREMOVE de DBT

El sistema difunde el evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo \_ o un elemento multimedia. Este mensaje es la última oportunidad para que las aplicaciones y los controladores se preparen para esta eliminación. Sin embargo, cualquier aplicación puede denegar esta solicitud y cancelar la operación.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEQUERYREMOVE y *lParam* establecidos como se describe a continuación.


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

Establezca en DBT \_ DEVICEQUERYREMOVE.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo que se quitará. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) de DEV y, a continuación, compruebe su **miembro \_ dbch devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para conceder permiso para quitar un dispositivo.

Devuelve BROADCAST \_ QUERY DENY para denegar el permiso para quitar un \_ dispositivo.

## <a name="remarks"></a>Observaciones

Debe cerrar todos los identificadores del dispositivo o se producirá un error en la eliminación del dispositivo.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [Procesamiento de una solicitud para quitar un dispositivo.](processing-a-request-to-remove-a-device.md)

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

 

 




