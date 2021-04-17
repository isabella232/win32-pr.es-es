---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento multimedia.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Evento DBT_DEVICEREMOVECOMPLETE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659543"
---
# <a name="dbt_deviceremovecomplete-event"></a>\_Evento DBT DEVICEREMOVECOMPLETE

El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento multimedia.

Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEREMOVECOMPLETE y *lParam* , tal y como se describe a continuación.


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

Establecer en DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo que se ha quitado. La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="remarks"></a>Observaciones

El sistema puede difundir un mensaje de DEVICEREMOVECOMPLETE de DBT \_ sin enviar mensajes [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) y [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondientes. En tales casos, las aplicaciones y los controladores deben recuperarse de la pérdida del dispositivo lo mejor posible.

Si se quita un medio, el tipo de dispositivo que llega a él es un volumen (el miembro **dbch \_ DEVICETYPE** es DBT \_ DEVTYP \_ ) y el cambio afecta a los medios (el miembro **dbcv \_ Flags** es DBTF \_ media).

## <a name="examples"></a>Ejemplos

Para ver un ejemplo, consulte detección de la [inserción o eliminación de medios](detecting-media-insertion-or-removal.md) o [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).

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

 

 




