---
description: El mensaje de QUERYENDSESSION de WM \_ se envía cuando el usuario elige finalizar la sesión o cuando una aplicación llama a una de las funciones de cierre del sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Mensaje de WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669781"
---
# <a name="wm_queryendsession-message"></a>Mensaje de QUERYENDSESSION de WM \_

El mensaje de **\_ QUERYENDSESSION de WM** se envía cuando el usuario elige finalizar la sesión o cuando una aplicación llama a una de las funciones de cierre del sistema. Si alguna aplicación devuelve cero, la sesión no finaliza. El sistema deja de enviar mensajes de **WM \_ QUERYENDSESSION** en cuanto una aplicación devuelve cero.

Después de procesar este mensaje, el sistema envía el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) con el parámetro *wParam* establecido en los resultados del mensaje de **\_ QUERYENDSESSION de WM** .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
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

Identificador **de \_ QUERYENDSESSION de WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes. Si este parámetro es 0, el sistema se está cerrando o reiniciando (no es posible determinar qué evento se está produciendo).



| Value                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x00000001</dt> </dl> | La aplicación está usando un archivo que debe reemplazarse, se está realizando el mantenimiento del sistema o se han agotado los recursos del sistema. Para obtener más información, consulte [directrices para aplicaciones](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> crítico </dl> | Se forzará el cierre de la aplicación.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LOGOFF**</dt> <dt>0x80000000</dt> </dl>       | El usuario está cerrando la sesión. Para obtener más información, consulte cerrar [sesión](logging-off.md).<br/>                                                                                                                                   |



 

Tenga en cuenta que este parámetro es una máscara de bits. Para probar este valor, use una operación de bits; no se comprueba la igualdad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Las aplicaciones deben respetar las intenciones del usuario y devolver **true**. De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **true** para este mensaje.

Si el apagado dañaría el sistema o el medio que se está grabando, la aplicación puede devolver el **valor false**. Sin embargo, se recomienda respetar las acciones del usuario.

## <a name="remarks"></a>Observaciones

Cuando una aplicación devuelve **true** para este mensaje, recibe el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) , sin tener en consideración el modo en que las otras aplicaciones responden al mensaje de **\_ QUERYENDSESSION de WM** . Cada aplicación debe devolver **true** o **false** inmediatamente después de recibir este mensaje y diferir las operaciones de limpieza hasta que reciba el mensaje de la **\_ ENDSESSION de WM** .

Las aplicaciones pueden mostrar una interfaz de usuario en la que se pide al usuario información al cerrarse; sin embargo, no se recomienda. Después de cinco segundos, el sistema muestra información acerca de las aplicaciones que están evitando el apagado y permite que el usuario las termine. Por ejemplo, Windows XP muestra un cuadro de diálogo, mientras que Windows Vista muestra una pantalla completa con información adicional sobre las aplicaciones que bloquean el cierre. Si la aplicación debe bloquear o posponer el cierre del sistema, use la función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . Para obtener más información, vea [cambios de apagado para Windows Vista](shutdown-changes-for-windows-vista.md).

Las aplicaciones de consola pueden utilizar la función [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para recibir la notificación de cierre.

Las aplicaciones de servicio pueden usar la función [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para recibir notificaciones de cierre en una rutina de controlador.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte cerrar [sesión](logging-off.md).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
