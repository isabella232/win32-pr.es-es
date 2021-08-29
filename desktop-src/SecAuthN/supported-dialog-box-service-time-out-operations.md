---
description: Winlogon implementa dos operaciones de tiempo de espera, una para cuadros de diálogo seguros y otra para la activación y finalización del protector de pantalla.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Operaciones de tiempo de espera de servicio de cuadro de diálogo admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7715cafb426a59bd9773791788dd9914fff0c1fac4a5b820e9cc06416e966eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916454"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Operaciones de tiempo de espera de servicio de cuadro de diálogo admitidas

[*Winlogon implementa*](../secgloss/w-gly.md) dos operaciones de tiempo de espera, una para cuadros de diálogo seguros y otra para la activación y finalización del protector de pantalla.

Al mostrar un cuadro de diálogo seguro, como iniciar sesión o desbloquear una estación de trabajo, Winlogon puede tiempo de espera de los cuadros de diálogo y devolver un código de resultado adecuado al procedimiento del cuadro de diálogo. Winlogon proporciona un conjunto de funciones de compatibilidad de cuadro de diálogo para [*GINA*](../secgloss/g-gly.md). GINA debe usar estas funciones en lugar de sus homólogos de Windows para asegurarse de que GINA y Winlogon mantienen el control adecuado sobre los cuadros de diálogo. Si no se usan las versiones de Winlogon de estas funciones, los usuarios no autorizados podrían obtener acceso al sistema.

Los servicios de cuadro de diálogo de Winlogon se proporcionan mediante las siguientes funciones de soporte técnico.



| Función de soporte técnico                                               | Descripción                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Similar a la Windows [**MessageBox.**](/windows/win32/api/winuser/nf-winuser-messagebox)                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Similar a la función Windows [**DialogBox.**](/windows/win32/api/winuser/nf-winuser-dialogboxa)                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Similar a la Windows [**dialogBoxIndirect.**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Similar a la Windows [**DialogBoxParam.**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Similar a la Windows [**dialogBoxIndirectParam.**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) |



 

Los archivos DLL de GINA también pueden recibir mensajes DE SAS de WLX \_ WM \_ de Winlogon. Estos mensajes se envían a cuadros de diálogo activos si se recibe una secuencia de [*atención*](../secgloss/s-gly.md) segura (SAS). Esto resulta útil si la GINA está en proceso de solicitar el PIN correspondiente [*para*](../secgloss/s-gly.md)una tarjeta inteligente y la tarjeta se quita del lector de [*tarjetas inteligentes.*](../secgloss/r-gly.md) Winlogon usa WLX DLG SAS como código de resultado EndDialog cuando se produce un evento \_ SAS durante una operación de cuadro de \_ diálogo.

Los tiempos de espera también se entregan de esta manera. Se envía un mensaje DE SAS DE WM de WLX con EL TIEMPO DE ESPERA DE SCRNSVR DE TIPO SAS de WLX o EL TIEMPO DE ESPERA \_ DE TIPO DE SAS de \_ \_ \_ \_ \_ \_ WLX. \_ \_ El cuadro de diálogo finalizará con un código de salida adecuado para permitir que los desarrolladores de GINA enlacen las notificaciones de tiempo de espera.

Winlogon puede finalizar los cuadros de diálogo de GINA mediante el código WLX \_ DLG \_ USER \_ LOGOFF. Esto indica que el usuario ha cerrado sesión durante la ejecución del cuadro de diálogo (por ejemplo, llamando a la [**función ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) desde otro subproceso).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados de Winlogon](winlogon-states.md)
</dt> <dt>

[Envío de mensajes a la GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Funciones de soporte técnico de Winlogon](authentication-functions.md)
</dt> </dl>

 

 
