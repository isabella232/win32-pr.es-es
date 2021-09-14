---
description: El sistema difunde el evento de dispositivo DBT DEVICEREMOVEPENDING cuando se quita un dispositivo o un elemento multimedia y ya no está \_ disponible para su uso.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: DBT_DEVICEREMOVEPENDING evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164453"
---
# <a name="dbt_deviceremovepending-event"></a>Evento \_ DBT DEVICEREMOVEPENDING

El sistema difunde el evento de dispositivo DBT DEVICEREMOVEPENDING cuando se quita un dispositivo o un elemento multimedia y ya no está \_ disponible para su uso.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ DEVICECHANGE**](wm-devicechange.md) de WM con *wParam* establecido en DBT \_ DEVICEREMOVEPENDING y *lParam* establecido como se describe a continuación.


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

Establezca en DBT \_ DEVICEREMOVEPENDING.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ \_ DEV BROADCAST HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

El sistema puede difundir un mensaje \_ DBT DEVICEREMOVEPENDING sin enviar un mensaje [ \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) de DBT correspondiente. En tales casos, las aplicaciones y los controladores deben recuperarse de la pérdida del dispositivo lo mejor posible.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [consulte Procesamiento de una solicitud para quitar un dispositivo.](processing-a-request-to-remove-a-device.md)

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

 

 




