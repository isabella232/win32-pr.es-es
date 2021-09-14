---
title: WM_RASDIALEVENT mensaje (Ras.h)
description: El sistema operativo envía un mensaje WM RASDIALEVENT a un procedimiento de ventana cuando se produce un evento de cambio de estado \_ durante un proceso de conexión RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT ras del mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073839"
---
# <a name="wm_rasdialevent-message"></a>Mensaje \_ RASDIALEVENT de WM

El sistema operativo envía un mensaje **\_ WM RASDIALEVENT** a un procedimiento de ventana cuando se produce un evento de cambio de estado durante un proceso de conexión RAS. Esto sucede cuando se ha especificado una ventana para controlar las notificaciones de estos eventos mediante el parámetro *notifier* de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Los dos parámetros de mensaje son equivalentes a los parámetros de los mismos nombres que se usan con las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valor de *wParam.* Equivalente al parámetro *rasconnstate* de las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Especifica un valor [**de enumerador RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) que indica el estado que el proceso de conexión de acceso remoto de RasDial está a punto de especificar.

</dd> <dt>

*dwError* 
</dt> <dd>

Valor de *lParam*. Equivalente al parámetro *dwError de* las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Un valor distinto de cero indica el error que se ha producido o cero si no se ha producido ningún error.

[**RasDial envía**](/windows/desktop/api/Ras/nf-ras-rasdiala) este mensaje con *dwError* establecido en cero tras la entrada a cada estado de conexión. Si se produce un error dentro de un estado, el mensaje se envía de nuevo para el estado, esta vez con un valor *dwError distinto de* cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Mensajes del servicio de acceso remoto](remote-access-service-messages.md)
</dt> <dt>

[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

