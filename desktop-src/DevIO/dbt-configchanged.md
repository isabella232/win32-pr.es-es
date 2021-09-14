---
description: El sistema difunde el evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un \_ acoplamiento o desacoplado. Una aplicación o controlador que almacena datos en el Registro bajo la clave HKEY \_ CURRENT CONFIG debe actualizar los \_ datos.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164482"
---
# <a name="dbt_configchanged-event"></a>Evento \_ CONFIGCHANGED de DBT

El sistema difunde el evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un \_ acoplamiento o desacoplado. Una aplicación o controlador que almacena datos en el Registro bajo la clave HKEY \_ CURRENT CONFIG debe actualizar los \_ datos.

Para difundir este evento de dispositivo, el sistema usa el mensaje [**\_ WM DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT CONFIGCHANGED y \_ *lParam* establecido en cero.


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

Establezca en DBT \_ CONFIGCHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Establecer en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




