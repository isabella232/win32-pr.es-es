---
description: En un protocolo de aplicación cliente/servidor, un servidor se enlaza a un puerto de comunicaciones como un socket o una interfaz RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Establecer una conexión segura con la autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649189"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Establecer una conexión segura con la autenticación

En un [*Protocolo de aplicación*](/windows/desktop/SecGloss/a-gly)cliente/servidor, un servidor se enlaza a un puerto de comunicaciones como un socket o una interfaz RPC. A continuación, el servidor espera a que un cliente se conecte y solicite el servicio. El rol de seguridad durante la configuración de la conexión es dos veces en el caso de la autenticación mutua:

-   Autenticación de cliente por el servidor.
-   Autenticación de servidor por el cliente.

Los componentes de cliente y servidor de una aplicación de transporte utilizan un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) para establecer una conexión segura para la transmisión de mensajes. El primer paso en el establecimiento de una conexión segura consiste en crear un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly). es decir, una estructura de datos opaca que contiene los datos de seguridad relevantes para una conexión, como una [*clave de sesión*](/windows/desktop/SecGloss/s-gly) y la duración de la sesión.

Un contexto de seguridad es esencialmente un mensaje del paquete de seguridad asociado al cliente al paquete de seguridad asociado al servidor. Por lo tanto, la creación de un contexto de seguridad normalmente requiere que tanto el cliente como el servidor realicen llamadas a sus respectivos paquetes de seguridad. Para obtener más información sobre las funciones de contexto, consulte [Administración de contexto](authentication-functions.md).

El protocolo que se usa para establecer una conexión segura y autenticada implica el intercambio de uno o más "tokens de seguridad" entre el cliente y el servidor. Estos tokens se envían como mensajes opacos por los dos lados junto con cualquier otra información específica del Protocolo de la [*aplicación*](/windows/desktop/SecGloss/a-gly). Como mensaje opaco, el cliente recibe el token de una función de paquete de seguridad, que no puede interpretarlo ni cambiarlo, y reenviarlo como un mensaje al servidor. El token también es opaco para el servidor, que no puede interpretar ni cambiar el token. El servidor reenvía el token opaco a su paquete de seguridad para su interpretación. A continuación, el paquete informa al servidor de la autenticación del cliente o de un error para autenticarse.

El cliente recibe el token del servidor en un mensaje, recupera el token del mensaje recibido y usa ese token en una llamada a su paquete de seguridad. Después, el cliente llama de nuevo al paquete de seguridad, lo que indica si se ha establecido una conexión segura o si es necesario realizar más intercambios antes de que una conexión segura esté lista. En teoría, no hay ningún límite en el número de intercambios de tokens de seguridad necesarios. En la práctica, solo se requiere un número limitado de intercambios. La autenticación NTLM se basa en el esquema de desafío/respuesta y utiliza tres lados para autenticar un cliente en el servidor. El protocolo [*Kerberos*](/windows/desktop/SecGloss/k-gly) versión 5,0 puede requerir intercambios de mensajes adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de contexto de cliente](client-context-initialization.md)
</dt> <dt>

[Inicialización de contexto de servidor](server-context-initialization.md)
</dt> </dl>

 

 
