---
title: Instrucciones para aplicaciones cliente/servidor
description: Las aplicaciones cliente/servidor no deben suponer que una conexión de un solo equipo es equivalente a una sesión de un solo usuario.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0c1a71256f3ab469bfeb1c08b2d096b56ac1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685720"
---
# <a name="clientserver-application-guidelines"></a>Instrucciones para aplicaciones cliente/servidor

Las aplicaciones cliente/servidor no deben suponer que una conexión de un solo equipo es equivalente a una sesión de un solo usuario. Este es un caso especial del problema descrito en [direcciones IP y nombres de equipo](ip-addresses-and-computer-names.md).

Para identificar de forma única una conexión cliente/servidor, cada módulo cliente debe usar un nombre o un identificador único. Las aplicaciones pueden usar objetos o canalizaciones con nombre, Sockets u otros métodos IPC. Para obtener más información, vea [espacios de nombres de objetos de kernel](kernel-object-namespaces.md).

Para que sea Servicios de Escritorio remoto compatible, el módulo de servidor en una aplicación cliente/servidor debe ser capaz de administrar varios clientes que se conectan desde el mismo equipo. Para ello, el módulo de servidor debe aceptar conexiones de cliente a través de una interfaz global bien definida, como RPC o canalizaciones con nombre. El servidor y el cliente deben negociar un canal de comunicación diferente para cada sesión de usuario. El cliente debe establecer una conexión con el servidor mediante el uso de protocolos que admiten fácilmente este tipo de operación, como TCP/IP, donde se puede usar una conexión de socket diferente para cada aplicación cliente.

El módulo cliente puede llamar a la función [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) para recuperar el identificador de su servicios de escritorio remoto sesión. Después, el cliente usa algún tipo de comunicación entre procesos para pasar su identificador de sesión al módulo del servidor. Los módulos de cliente y servidor pueden usar el identificador de sesión para configurar un canal de comunicación privado. Por ejemplo, el módulo de servidor puede usar un identificador de sesión para tener acceso a los objetos del espacio de nombres de la sesión para los objetos de kernel.

Además, el módulo de servidor puede usar el identificador de sesión en una llamada a [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) para recuperar información adicional sobre el cliente. El módulo de servidor también puede usar el identificador de sesión en una llamada a [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) para mostrar un mensaje en el terminal del cliente. El módulo servidor también puede crear dos eventos para supervisar la conexión de cliente y desconectarse de una sesión. Sin embargo, debe estar registrado en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) para ello. Para obtener más información, vea [supervisar conexiones y desconexiones de sesión](monitoring-session-connections-and-disconnections.md).

Los mensajes de entrada del usuario son una posible fuente de problemas para las aplicaciones cliente/servidor. Por ejemplo, si un servicio llama a la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) , el cuadro de mensaje se muestra en el escritorio del servidor host de sesión de escritorio remoto, no en el escritorio del cliente. Para mostrar un mensaje en un escritorio cliente, el servicio puede llamar a la función [**WtsSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) . Como alternativa, el servicio puede solicitar la entrada del módulo cliente y el módulo cliente puede mostrar la interfaz de usuario y enviar la entrada resultante de vuelta al servicio.

Los procesos generados a partir de varias sesiones pueden enviar y recibir datos entre sí mediante el uso de bloques de memoria compartida. Para obtener más información, consulte [crear memoria compartida con nombre](/windows/desktop/Memory/creating-named-shared-memory). No se puede usar la memoria compartida en las siguientes condiciones:

-   Varias sesiones generaron los procesos que usan el bloque de memoria compartida.
-   Las sesiones comparten las mismas credenciales de autenticación de usuario.

 

 