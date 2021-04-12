---
description: El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un acoplamiento o desacoplamiento. Una aplicación o un controlador que almacene datos en el registro con la clave de configuración de HKEY \_ Current \_ debe actualizar los datos.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Evento DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274958"
---
# <a name="dbt_configchanged-event"></a>\_Evento DBT CONFIGCHANGED

El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un acoplamiento o desacoplamiento. Una aplicación o un controlador que almacene datos en el registro con la clave de configuración de HKEY \_ Current \_ debe actualizar los datos.

Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ CONFIGCHANGED y *lParam* establecido en cero.


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

Establézcalo en DBT \_ CONFIGCHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Establecer en cero.

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

[**DEVICECHANGE de WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




