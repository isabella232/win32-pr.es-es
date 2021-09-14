---
description: Winlogon envía mensajes a la GINA mientras se muestran los cuadros de diálogo. Todos estos mensajes se encapsulan en el mensaje DE SAS de WLX \_ WM como se indica a \_ continuación.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envío de mensajes a la GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173377"
---
# <a name="sending-messages-to-the-gina"></a>Envío de mensajes a la GINA

[*Winlogon envía*](../secgloss/w-gly.md) mensajes a [*la GINA mientras*](../secgloss/g-gly.md) se muestran los cuadros de diálogo. Todos estos mensajes se encapsulan en el mensaje DE SAS de WLX \_ WM como se indica a \_ continuación.



| Tipo de secuencia de atención segura en el parámetro wParam | Descripción                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ SAS \_ TYPE \_ CTRL \_ ALT \_ DEL                     | Indica que se recibió una secuencia de claves CTRL+ALT+SUPR.                                                                                      |
| WLX \_ SAS \_ TYPE \_ SC \_ INSERT                         | Indica que se [*ha insertado una*](../secgloss/s-gly.md) tarjeta inteligente en un dispositivo compatible. |
| WLX \_ SAS \_ TYPE \_ SC \_ REMOVE                         | Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.                                                                        |
| CIERRE DE \_ SESIÓN DE USUARIO DE TIPO SAS \_ \_ \_ DE WLX                       | Indica que un usuario solicitó el cierre de sesión.                                                                                                       |
| TIEMPO DE ESPERA \_ DE \_ \_ SCRNSVR DE TIPO SAS \_ DE WLX                   | Indica que el protector de pantalla debe ejecutarse debido a la falta de entrada del usuario.                                                                      |
| TIEMPO DE ESPERA \_ DE TIPO DE SAS \_ DE WLX \_                            | Indica que no se recibió ninguna entrada del usuario dentro del período de tiempo de espera especificado.                                                               |



 

Para los tiempos de espera y los cierres de sesión, Winlogon cerrará el cuadro de diálogo una vez enviado el mensaje. Este mensaje se envía para que la operación del cuadro de diálogo pueda responder de una manera útil (por ejemplo, cerrando si se ha producido un cierre de sesión).

Para los tiempos de espera de entrada, el cuadro de diálogo se cierra con el código TIEMPO DE ESPERA \_ DE ENTRADA DLG DE \_ WLX. \_

En el caso de los tiempos de espera del protector de pantalla, el cuadro de diálogo se cierra con el código WLX \_ DLG \_ SCREEN SAVER \_ \_ TIMEOUT.

En el caso de los cierres de sesión, la operación del cuadro de diálogo se cierra con el código WLX \_ DLG \_ USER \_ LOGOFF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados de Winlogon](winlogon-states.md)
</dt> <dt>

[Operaciones de tiempo de espera de servicio de cuadro de diálogo admitidas](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Funciones de soporte técnico de Winlogon](authentication-functions.md)
</dt> </dl>

 

 
