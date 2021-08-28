---
description: La función ExitWindows cierra la sesión del usuario actual. También puede llamar a la función ExitWindowsEx con la marca \_ EXW LOGOFF.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Cerrar sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ab8525630673b897704cea675c5c2a1e6dc6b1df4dd875e8872a79f915204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664405"
---
# <a name="logging-off"></a>Cerrar sesión

La [**función ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) cierra la sesión del usuario actual. También puede llamar a la [**función ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con la marca \_ EXW LOGOFF.

De forma predeterminada, cuando una aplicación usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión, el sistema envía el mensaje [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a cada ventana. Las aplicaciones aceptan finalizar devolviendo **TRUE** cuando reciben este mensaje. Si alguna aplicación devuelve **FALSE al** procesar este mensaje, se cancela la operación de cierre de sesión. Si la aplicación controla el mensaje **WM \_ QUERYENDSESSION,** puede permitir que el usuario cancele la operación de cierre de sesión, incluso si otra aplicación o el sistema originó la solicitud de la sesión final. Para obtener un ejemplo, [vea Cómo cerrar la sesión del usuario actual.](how-to-log-off-the-current-user.md)

Cuando una aplicación devuelve **TRUE** para [**WM \_ QUERYENDSESSION,**](wm-queryendsession.md)recibe el mensaje [**WM \_ ENDSESSION**](wm-endsession.md) y finaliza, independientemente de cómo respondan las otras aplicaciones al **mensaje WM \_ QUERYENDSESSION.**

Para forzar la terminación de todas las aplicaciones, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)y especifique la marca EXW \_ FORCE. Esto evita que el sistema envíe [**mensajes \_ WM QUERYENDSESSION.**](wm-queryendsession.md)

El sistema también envía la señal de control CTRL \_ LOGOFF \_ EVENT a cada proceso durante una operación de cierre de sesión. Una aplicación de consola puede registrar [**un HandlerRoutine**](/windows/console/handlerroutine) para procesar estos mensajes.

Si el proceso llamado [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) se ejecuta en la sesión de inicio de sesión del usuario interactivo, se finalizan todos los procesos de la sesión de inicio de sesión. Si el proceso que llama **a ExitWindowsEx** está en alguna otra sesión de inicio de sesión, solo se realizan las notificaciones; no se termina ningún proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo cerrar la sesión del usuario actual](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
