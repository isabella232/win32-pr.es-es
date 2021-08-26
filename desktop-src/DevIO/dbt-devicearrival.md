---
description: El sistema difunde el evento de dispositivo DBT DEVICEARRIVAL cuando se ha insertado un dispositivo o un elemento multimedia y \_ está disponible.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: DBT_DEVICEARRIVAL evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 826d0b510ca76b829eb683396c99579c14a512a6773b76a2049ae7963ede54a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088155"
---
# <a name="dbt_devicearrival-event"></a>Evento \_ DEVICEARRIVAL de DBT

El sistema difunde el evento de dispositivo DBT DEVICEARRIVAL cuando se ha insertado un dispositivo o un elemento multimedia y \_ está disponible.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ WM DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEARRIVAL y *lParam* establecidos como se describe a continuación.


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

Establezca en DBT \_ DEVICEARRIVAL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo insertado. La estructura consta de un encabezado independiente del evento, seguido de miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una estructura [**\_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) de DEV y, a continuación, compruebe su **miembro \_ dbch devicetype** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

Si se insertan medios, el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ devicetype** es DBT DEVTYP VOLUME) y el cambio afecta al medio (el miembro \_ \_ **dbcv \_ flags** es DBTF \_ MEDIA).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Detectar inserción o eliminación de medios.](detecting-media-insertion-or-removal.md)

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

 

 




