---
title: Mensaje de WM_RASDIALEVENT (RAS. h)
description: El sistema operativo envía un \_ mensaje de WM RASDIALEVENT a un procedimiento de ventana cuando se produce un cambio de evento de estado durante un proceso de conexión RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT el mensaje RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676565"
---
# <a name="wm_rasdialevent-message"></a>Mensaje de RASDIALEVENT de WM \_

El sistema operativo envía un mensaje de **WM \_ RASDIALEVENT** a un procedimiento de ventana cuando se produce un cambio de evento de estado durante un proceso de conexión RAS. Esto sucede cuando se ha especificado una ventana para controlar las notificaciones de estos eventos mediante el parámetro de *notificador* de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Los dos parámetros de mensaje son equivalentes a los parámetros de los mismos nombres que se usan con las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valor de *wParam*. Equivalente al parámetro *rasconnstate* de las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Especifica un valor de enumerador [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) que indica el estado que está a punto de entrar en el proceso de conexión de acceso remoto rasdial.

</dd> <dt>

*dwError* 
</dt> <dd>

Valor de *lParam*. Equivalente al parámetro *dwError* de las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Un valor distinto de cero indica el error que se ha producido, o cero si no se ha producido ningún error.

[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envía este mensaje con el valor de *dwError* establecido en cero cuando se entra en cada estado de conexión. Si se produce un error dentro de un estado, el mensaje se envía de nuevo para el estado, esta vez con un valor *dwError* distinto de cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Ras. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Mensajes del servicio de acceso remoto](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

