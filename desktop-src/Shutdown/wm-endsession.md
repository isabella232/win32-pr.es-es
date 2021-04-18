---
description: El \_ mensaje ENDSESSION de WM se envía a una aplicación después de que el sistema procese los resultados del mensaje de QUERYENDSESSION de WM \_ . El \_ mensaje ENDSESSION de WM informa a la aplicación de si la sesión está finalizando.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Mensaje de WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666714"
---
# <a name="wm_endsession-message"></a>\_Mensaje ENDSESSION de WM

El **mensaje \_ ENDSESSION de WM** se envía a una aplicación después de que el sistema procese los resultados del mensaje de [**\_ QUERYENDSESSION de WM**](wm-queryendsession.md) . El **mensaje \_ ENDSESSION de WM** informa a la aplicación de si la sesión está finalizando.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador **\_ ENDSESSION de WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Si se finaliza la sesión, este parámetro es **true**; la sesión puede finalizar en cualquier momento después de que todas las aplicaciones hayan devuelto el procesamiento de este mensaje. De lo contrario, es **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes. Si este parámetro es 0, el sistema se está cerrando o reiniciando (no es posible determinar qué evento se está produciendo).



| Value                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x1</dt> </dl>        | Si *wParam* es **true**, la aplicación debe cerrarse. Los datos deben guardarse automáticamente sin preguntar al usuario (para obtener más información, vea la sección comentarios). El administrador de reinicio envía este mensaje cuando la aplicación está usando un archivo que necesita ser reemplazado, cuando debe atender el sistema o cuando se agotan los recursos del sistema. La aplicación se reiniciará si se ha registrado para el reinicio mediante la función [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . Para obtener más información, consulte [directrices para aplicaciones](../rstmgr/guidelines-for-applications.md). <br/> Si *wParam* es **false**, la aplicación no se debe cerrar.<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> crítico </dl> | Se forzará el cierre de la aplicación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LOGOFF**</dt> <dt>0x80000000</dt> </dl>       | El usuario está cerrando la sesión. Para obtener más información, consulte cerrar [sesión](logging-off.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Tenga en cuenta que este parámetro es una máscara de bits. Para probar este valor, use una operación de bits; no se comprueba la igualdad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Las aplicaciones que tienen datos no guardados pueden guardar los datos en una ubicación temporal y restaurarlos la próxima vez que se inicie la aplicación. Se recomienda que las aplicaciones guarden los datos y el estado con frecuencia. por ejemplo, guarde automáticamente los datos entre las operaciones de guardado iniciadas por el usuario para reducir la cantidad de datos que se van a guardar en el cierre.

La aplicación no necesita llamar a la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) o [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) cuando finaliza la sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]<br/>                                                       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Cerrando sesión](logging-off.md)
</dt> <dt>

[Apagar](shutting-down.md)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**QUERYENDSESSION de WM \_**](wm-queryendsession.md)
</dt> </dl>

 

 
