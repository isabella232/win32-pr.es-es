---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICETYPESPECIFIC cuando se produce un evento específico del dispositivo.
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: Evento DBT_DEVICETYPESPECIFIC (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d7820f5769c6edd3a48b58073b55a911dae862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907220"
---
# <a name="dbt_devicetypespecific-event"></a>\_Evento DBT DEVICETYPESPECIFIC

El sistema difunde el \_ evento de dispositivo DBT DEVICETYPESPECIFIC cuando se produce un evento específico del dispositivo.

Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICETYPESPECIFIC y *lParam* , tal y como se describe a continuación.


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

Establézcalo en DBT \_ DEVICETYPESPECIFIC.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que identifica el dispositivo. La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo. Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

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

 

 




