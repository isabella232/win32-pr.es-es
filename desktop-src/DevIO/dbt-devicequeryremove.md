---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo o un elemento multimedia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Evento DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659544"
---
# <a name="dbt_devicequeryremove-event"></a>\_Evento DBT DEVICEQUERYREMOVE

El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo o un elemento multimedia. Este mensaje es la última oportunidad para que las aplicaciones y los controladores se preparen para esta eliminación. Sin embargo, cualquier aplicación puede denegar esta solicitud y cancelar la operación.

Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEQUERYREMOVE y *lParam* , tal y como se describe a continuación.


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

Establézcalo en DBT \_ DEVICEQUERYREMOVE.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo que se va a quitar. La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para conceder permiso para quitar un dispositivo.

Devolver consulta de difusión \_ \_ denegar para denegar el permiso para quitar un dispositivo.

## <a name="remarks"></a>Observaciones

Debe cerrar todos los identificadores del dispositivo o se producirá un error en la eliminación del dispositivo.

## <a name="examples"></a>Ejemplos

Para ver un ejemplo, consulte [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).

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

[**DEV \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**DEVICECHANGE de WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




