---
title: Directrices de aplicación cliente/servidor
description: Las aplicaciones cliente/servidor no deben asumir que una sola conexión de equipo es equivalente a una sesión de usuario único.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d27f5bd024e2311307f39e4f86584747b59b874576e5cd5aa28e735b2945d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001623"
---
# <a name="clientserver-application-guidelines"></a>Directrices de aplicación cliente/servidor

Las aplicaciones cliente/servidor no deben asumir que una sola conexión de equipo es equivalente a una sesión de usuario único. Se trata de un caso especial del problema que se describe en Direcciones [IP y nombres de equipo.](ip-addresses-and-computer-names.md)

Para identificar de forma única una conexión de cliente/servidor, cada módulo de cliente debe usar un nombre o identificador únicos. Las aplicaciones pueden usar objetos con nombre, canalizaciones, sockets u otros métodos IPC. Para obtener más información, vea [Kernel Object Namespaces](kernel-object-namespaces.md).

Para que Servicios de Escritorio remoto, el módulo de servidor de una aplicación cliente/servidor debe ser capaz de controlar varios clientes que se conectan desde el mismo equipo. Para ello, el módulo de servidor debe aceptar conexiones de cliente a través de una interfaz global bien definida, como RPC o canalizaciones con nombre. El servidor y el cliente deben negociar un canal de comunicación diferente para cada sesión de usuario. El cliente debe establecer una conexión al servidor mediante protocolos que admitan fácilmente este tipo de operación, como TCP/IP, donde se puede usar una conexión de socket diferente para cada aplicación cliente.

El módulo cliente puede llamar a [**la función ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) para recuperar el identificador de su Servicios de Escritorio remoto sesión. A continuación, el cliente usa algún tipo de comunicación entre procesos para pasar su identificador de sesión al módulo del servidor. Los módulos de cliente y servidor pueden usar el identificador de sesión para configurar un canal de comunicación privado. Por ejemplo, el módulo de servidor puede usar un identificador de sesión para tener acceso a los objetos del espacio de nombres de la sesión para los objetos de kernel.

Además, el módulo de servidor puede usar el identificador de sesión en una [**llamada WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) para recuperar información adicional sobre el cliente. El módulo de servidor también puede usar el identificador de sesión en una [**llamada WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) para mostrar un mensaje en el terminal cliente. El módulo de servidor también puede crear dos eventos para supervisar la conexión del cliente y la desconexión de una sesión. Sin embargo, debe registrarse en el Escritorio remoto host de sesión (host de sesión de Escritorio remoto) para ello. Para obtener más información, vea [Supervisión de conexiones y desconexiones de sesión.](monitoring-session-connections-and-disconnections.md)

Las solicitudes de entrada del usuario son una posible fuente de problemas para las aplicaciones cliente/servidor. Por ejemplo, si un servicio llama a la función [**MessageBox,**](/windows/desktop/api/winuser/nf-winuser-messagebox) el cuadro de mensaje se muestra en el escritorio del servidor host de sesión de Escritorio remoto, no en el escritorio del cliente. Para mostrar un mensaje en un escritorio cliente, el servicio puede llamar a la [**función WtsSendMessage.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) Como alternativa, el servicio puede solicitar la entrada del módulo cliente y el módulo cliente puede mostrar la interfaz de usuario y enviar la entrada resultante al servicio.

Los procesos generados a partir de varias sesiones pueden enviar datos y recibir datos entre sí mediante el uso de bloques de memoria compartida. Para obtener más información, vea [Crear memoria compartida con nombre.](/windows/desktop/Memory/creating-named-shared-memory) La memoria compartida no se puede usar en las siguientes condiciones:

-   Varias sesiones generaron los procesos que usan el bloque de memoria compartida.
-   Las sesiones comparten la misma credencial de autenticación de usuario.

 

 