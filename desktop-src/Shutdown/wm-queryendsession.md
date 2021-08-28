---
description: El mensaje WM QUERYENDSESSION se envía cuando el usuario elige finalizar la sesión o cuando una aplicación \_ llama a una de las funciones de apagado del sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: WM_QUERYENDSESSION mensaje (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6807a861ffb0670013a1d1f5b98a2f202e5d7470a6c306b3ed29c42baad6e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664215"
---
# <a name="wm_queryendsession-message"></a>Mensaje \_ DE WM QUERYENDSESSION

El **mensaje \_ WM QUERYENDSESSION** se envía cuando el usuario elige finalizar la sesión o cuando una aplicación llama a una de las funciones de apagado del sistema. Si alguna aplicación devuelve cero, la sesión no finaliza. El sistema deja de enviar **mensajes \_ WM QUERYENDSESSION** en cuanto una aplicación devuelve cero.

Después de procesar este mensaje, el sistema envía el mensaje [**\_ WM ENDSESSION**](wm-endsession.md) con el parámetro *wParam* establecido en los resultados del **mensaje WM \_ QUERYENDSESSION.**

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador **DE WM \_ QUERYENDSESSION.**

</dd> <dt>

*wParam* 
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes. Si este parámetro es 0, el sistema se está cerrando o reiniciando (no es posible determinar qué evento se está produciendo).



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CloseAPP**</dt> <dt>0x00000001</dt> </dl> | La aplicación usa un archivo que se debe reemplazar, el sistema se está atendidas o se agotan los recursos del sistema. Para obtener más información, vea [Directrices para aplicaciones.](../rstmgr/guidelines-for-applications.md)<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_ Crítico**</dt> <dt>0x40000000</dt> </dl> | La aplicación se ve forzada a cerrarse.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LogOFF**</dt> <dt>0x80000000</dt> </dl>       | El usuario está iniciando sesión. Para obtener más información, [vea Cerrar sesión.](logging-off.md)<br/>                                                                                                                                   |



 

Tenga en cuenta que este parámetro es una máscara de bits. Para probar este valor, use una operación bit a bit; no pruebe la igualdad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Las aplicaciones deben respetar las intenciones del usuario y devolver **TRUE.** De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **TRUE** para este mensaje.

Si apagar dañaría el sistema o los medios que se están dañando, la aplicación puede devolver **FALSE**. Sin embargo, es un procedimiento recomendado respetar las acciones del usuario.

## <a name="remarks"></a>Comentarios

Cuando una aplicación devuelve **TRUE** para este mensaje, recibe el mensaje [**WM \_ ENDSESSION,**](wm-endsession.md) independientemente de cómo respondan las otras aplicaciones al mensaje **DE WM \_ QUERYENDSESSION.** Cada aplicación debe devolver **TRUE** o **FALSE inmediatamente** después de recibir este mensaje y aplazar las operaciones de limpieza hasta que reciba el mensaje **WM \_ ENDSESSION.**

Las aplicaciones pueden mostrar una interfaz de usuario que solicita al usuario información durante el apagado, pero no se recomienda. Después de cinco segundos, el sistema muestra información sobre las aplicaciones que impiden el apagado y permite al usuario finalizarlas. Por ejemplo, Windows XP muestra un cuadro de diálogo, mientras que Windows Vista muestra una pantalla completa con información adicional sobre las aplicaciones que bloquean el cierre. Si la aplicación debe bloquear o posponer el apagado del sistema, use la [**función ShutdownBlockReasonCreate.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) Para obtener más información, vea [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Las aplicaciones de consola pueden usar [**la función SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para recibir una notificación de apagado.

Las aplicaciones de servicio pueden usar [**la función RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para recibir notificaciones de cierre en una rutina de controlador.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Cerrar sesión.](logging-off.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                                       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                              |
| Header<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Cerrar sesión](logging-off.md)
</dt> <dt>

[Cerrando](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
