---
description: El sistema difunde el evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento \_ multimedia.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5998742d823d710bfb91cd10579a3fb1ec65bec42b615fc7fdac3ac35545b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539195"
---
# <a name="dbt_deviceremovecomplete-event"></a>Evento \_ DBT DEVICEREMOVECOMPLETE

El sistema difunde el evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento \_ multimedia.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEREMOVECOMPLETE y *lParam* establecido como se describe a continuación.


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

Se establece en DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo quitado. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ \_ DEV BROADCAST HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

El sistema puede difundir un mensaje DBT DEVICEREMOVECOMPLETE sin enviar los mensajes \_ [ \_ DBT DEVICEQUERYREMOVE](dbt-devicequeryremove.md) y [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondientes. En tales casos, las aplicaciones y los controladores deben recuperarse de la pérdida del dispositivo lo mejor posible.

Si se quitan medios, el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ devicetype** es DBT DEVTYP VOLUME) y el cambio afecta a los medios (el miembro \_ \_ **dbcv \_ flags** es DBTF \_ MEDIA).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Detectar inserción o](detecting-media-insertion-or-removal.md) eliminación de medios o [Procesar una solicitud para quitar un dispositivo.](processing-a-request-to-remove-a-device.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




