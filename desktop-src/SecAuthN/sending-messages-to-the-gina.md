---
description: Winlogon envía mensajes a GINA mientras se muestran los cuadros de diálogo. Todos estos mensajes se encapsulan en el mensaje DE SAS de WLX \_ WM como se indica a \_ continuación.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envío de mensajes a la GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb52da6a2a66d901207485ed97592a97286902ba51c54ec4924240ab9403a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918326"
---
# <a name="sending-messages-to-the-gina"></a>Envío de mensajes a la GINA

[*Winlogon envía*](../secgloss/w-gly.md) mensajes a [*la GINA mientras*](../secgloss/g-gly.md) se muestran los cuadros de diálogo. Todos estos mensajes se encapsulan en el mensaje DE SAS de WLX \_ WM como se indica a \_ continuación.



| Tipo de secuencia de atención segura en el parámetro wParam | Descripción                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ SAS TYPE CTRL ALT \_ \_ \_ \_ SUPR                     | Indica que se recibió una secuencia de claves CTRL+ALT+SUPR.                                                                                      |
| WLX \_ SAS \_ TYPE \_ SC \_ INSERT                         | Indica que se [*ha insertado una tarjeta*](../secgloss/s-gly.md) inteligente en un dispositivo compatible. |
| WLX \_ SAS \_ TYPE \_ SC \_ REMOVE                         | Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.                                                                        |
| WLX \_ SAS \_ TYPE \_ USER \_ LOGOFF                       | Indica que un usuario solicitó el cierre de sesión.                                                                                                       |
| TIEMPO DE ESPERA \_ DE WLX SAS \_ TYPE \_ SCRNSVR \_                   | Indica que el protector de pantalla debe ejecutarse debido a la falta de entrada del usuario.                                                                      |
| TIEMPO DE ESPERA \_ DE TIPO DE SAS \_ \_ DE WLX                            | Indica que no se recibió ninguna entrada del usuario dentro del período de tiempo de espera especificado.                                                               |



 

Para los tiempos de espera y los cierres de sesión, Winlogon cerrará el cuadro de diálogo después de que se haya enviado el mensaje. Este mensaje se envía para que la operación del cuadro de diálogo pueda responder de una manera útil (por ejemplo, cerrando si se ha producido un cierre de sesión).

Para los tiempos de espera de entrada, el cuadro de diálogo se cierra con el código WLX \_ DLG \_ INPUT \_ TIMEOUT.

Para los tiempos de espera del protector de pantalla, el cuadro de diálogo se cierra con el código WLX \_ DLG \_ SCREEN SAVER \_ \_ TIMEOUT.

Para los cierres de sesión, la operación del cuadro de diálogo se cierra con el código WLX \_ DLG \_ USER \_ LOGOFF.

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

 

 
