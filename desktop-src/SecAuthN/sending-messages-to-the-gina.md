---
description: Winlogon envía mensajes a GINA mientras se muestran los cuadros de diálogo. Estos mensajes se encapsulan en el \_ mensaje SAS de WLX WM \_ como se indica a continuación.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envío de mensajes a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667113"
---
# <a name="sending-messages-to-the-gina"></a>Envío de mensajes a GINA

[*Winlogon*](../secgloss/w-gly.md) envía mensajes a [*Gina*](../secgloss/g-gly.md) mientras se muestran los cuadros de diálogo. Estos mensajes se encapsulan en el \_ mensaje SAS de WLX WM \_ como se indica a continuación.



| Tipo de secuencia de atención segura en el parámetro wParam | Descripción                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ tipo de SAS \_ \_ Ctrl \_ ALT \_ Supr                     | Indica que se ha recibido una secuencia de teclas CTRL + ALT + SUPR.                                                                                      |
| WLX \_ SAS \_ Type \_ SC \_ Insert                         | Indica que se ha insertado una [*tarjeta inteligente*](../secgloss/s-gly.md) en un dispositivo compatible. |
| WLX \_ SAS \_ tipo \_ SC \_ Remove                         | Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.                                                                        |
| \_cierre de \_ \_ sesión de usuario de tipo SAS de WLX \_                       | Indica que un usuario solicitó el cierre de sesión.                                                                                                       |
| WLX \_ tipo de SAS \_ \_ SCRNSVR \_ tiempo de espera                   | Indica que se debe ejecutar el protector de pantalla debido a la falta de intervención del usuario.                                                                      |
| WLX \_ \_ tiempo de espera de tipo SAS \_                            | Indica que no se ha recibido ninguna entrada de usuario dentro del período de tiempo de espera especificado.                                                               |



 

En el caso de los tiempos de espera y cierres de sesión, Winlogon cerrará el cuadro de diálogo después de enviar el mensaje. Este mensaje se envía para que la operación del cuadro de diálogo pueda responder de una manera útil (por ejemplo, al cerrarse si se ha producido un cierre de sesión).

En el caso de los tiempos de espera de entrada, el cuadro de diálogo se cierra con el tiempo de espera de entrada de Code WLX \_ Dlg \_ \_ .

En el caso de los tiempos de espera del protector de pantalla, el cuadro de diálogo se cierra con el tiempo de espera del protector de pantalla Code WLX \_ Dlg \_ \_ \_ .

Para los cierres de sesión, la operación del cuadro de diálogo se cierra con el código WLX \_ Dlg \_ cierre de sesión del usuario \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicializando Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados de Winlogon](winlogon-states.md)
</dt> <dt>

[Cuadro de diálogo compatible Tiempo de servicio operaciones de salida](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Funciones de compatibilidad con Winlogon](authentication-functions.md)
</dt> </dl>

 

 
