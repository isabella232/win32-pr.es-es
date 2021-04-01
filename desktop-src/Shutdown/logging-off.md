---
description: La función ExitWindows cierra la sesión del usuario actual. También puede llamar a la función ExitWindowsEx con la \_ marca de cierre de sesión EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Cerrando sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913850"
---
# <a name="logging-off"></a>Cerrando sesión

La función [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) cierra la sesión del usuario actual. También puede llamar a la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con la \_ marca de cierre de sesión EXW.

De forma predeterminada, cuando una aplicación usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión, el sistema envía el mensaje de [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a cada ventana. Las aplicaciones aceptan finalizar devolviendo **true** cuando reciben este mensaje. Si alguna aplicación devuelve **false** al procesar este mensaje, se cancela la operación de cierre de sesión. Si la aplicación controla el mensaje de **\_ QUERYENDSESSION de WM** , puede permitir que el usuario cancele la operación de cierre de sesión, incluso si otra aplicación o el sistema originó la solicitud de la sesión final. Para obtener un ejemplo, consulte [cómo cerrar la sesión del usuario actual](how-to-log-off-the-current-user.md).

Cuando una aplicación devuelve **true** para [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), recibe el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) y se termina, independientemente de cómo respondan las otras aplicaciones al mensaje **de \_ QUERYENDSESSION de WM** .

Para forzar la finalización de todas las aplicaciones, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)y especifique la \_ marca Force de EXW. Esto impide que el sistema envíe mensajes de [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .

El sistema también envía la \_ señal de control de evento Ctrl Logoff \_ a todos los procesos durante una operación de cierre de sesión. Una aplicación de consola puede registrar un [**HandlerRoutine**](/windows/console/handlerroutine) para procesar estos mensajes.

Si el proceso que llamó a [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) se está ejecutando en la sesión de inicio de sesión del usuario interactivo, se finalizan todos los procesos de la sesión de inicio de sesión. Si el proceso que llama a **ExitWindowsEx** está en otra sesión de inicio de sesión, solo se realizan las notificaciones; no se termina ningún proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo cerrar la sesión del usuario actual](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
