---
description: Winlogon implementa dos operaciones de tiempo de espera, una para los cuadros de diálogo seguros y la otra para la activación y finalización del protector de pantalla.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Cuadro de diálogo compatible Tiempo de servicio operaciones de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809901"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Cuadro de diálogo compatible Tiempo de servicio operaciones de salida

[*Winlogon*](../secgloss/w-gly.md) implementa dos operaciones de tiempo de espera, una para los cuadros de diálogo seguros y la otra para la activación y finalización del protector de pantalla.

Al mostrar un cuadro de diálogo seguro, como el inicio de sesión o el desbloqueo de una estación de trabajo, Winlogon puede agotar el tiempo de espera de los cuadros de diálogo y devolver un código de resultado adecuado al procedimiento del cuadro de diálogo. Winlogon proporciona un conjunto de funciones de compatibilidad de cuadro de diálogo para [*Gina*](../secgloss/g-gly.md). GINA debe usar estas funciones en lugar de sus homólogos de Windows para asegurarse de que GINA y Winlogon mantienen el control adecuado sobre los cuadros de diálogo. Si no se utilizan las versiones de Winlogon de estas funciones, los usuarios no autorizados tendrán acceso al sistema.

Los servicios del cuadro de diálogo Winlogon se proporcionan mediante las siguientes funciones de soporte técnico.



| Función de soporte técnico                                               | Descripción                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Similar a la función [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) de Windows.                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Similar a la función [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) de Windows.                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Similar a la función [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) de Windows.           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Similar a la función [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) de Windows.                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Similar a la función [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) de Windows. |



 

Los archivos dll de GINA también pueden recibir \_ \_ mensajes SAS de WLX WM desde Winlogon. Estos mensajes se envían a los cuadros de diálogo activos si se recibe una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS). Esto resulta útil si GINA está en proceso de solicitar el PIN correspondiente para una [*tarjeta inteligente*](../secgloss/s-gly.md)y la tarjeta se quita del [*lector*](../secgloss/r-gly.md)de tarjeta inteligente. Winlogon usa \_ SAS WLX Dlg \_ como código de resultado EndDialog cuando se produce un evento de SAS durante una operación de cuadro de diálogo.

Los tiempos de espera también se entregan de esta manera. \_Se envía un mensaje SAS de WLX WM con el tiempo de espera de \_ WLX de \_ \_ tipo SAS \_ SCRNSVR o de \_ WLX \_ \_ \_ . El cuadro de diálogo finalizará con un código de salida adecuado para permitir a los desarrolladores de GINA enlazar las notificaciones de tiempo de espera.

Winlogon puede finalizar los cuadros de diálogo de GINA mediante el código de \_ cierre de sesión de usuario WLX Dlg \_ \_ . Esto indica que el usuario ha cerrado la sesión durante la ejecución del cuadro de diálogo (por ejemplo, mediante una llamada a la función [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) desde otro subproceso).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicializando Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados de Winlogon](winlogon-states.md)
</dt> <dt>

[Envío de mensajes a GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Funciones de compatibilidad con Winlogon](authentication-functions.md)
</dt> </dl>

 

 
