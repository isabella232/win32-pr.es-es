---
description: En un protocolo de aplicación cliente/servidor, un servidor se enlaza a un puerto de comunicación, como un socket o una interfaz RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Establecimiento de una conexión segura con autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271444"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Establecimiento de una conexión segura con autenticación

En un protocolo de aplicación [*cliente/servidor*](/windows/desktop/SecGloss/a-gly), un servidor enlaza a un puerto de comunicación, como un socket o una interfaz RPC. A continuación, el servidor espera a que un cliente se conecte y solicite el servicio. El rol de seguridad en la configuración de la conexión es doble en el caso de la autenticación mutua:

-   Autenticación de cliente por el servidor.
-   Autenticación del servidor por parte del cliente.

Los componentes de cliente y servidor de una aplicación de transporte usan un paquete [*de seguridad*](/windows/desktop/SecGloss/s-gly) para establecer una conexión segura para transmitir mensajes. El primer paso para establecer una conexión segura es crear un contexto [*de seguridad*](/windows/desktop/SecGloss/s-gly); es decir, una estructura de datos opaca que contiene los datos de seguridad pertinentes [*para*](/windows/desktop/SecGloss/s-gly) una conexión, como una clave de sesión y la duración de la sesión.

Un contexto de seguridad es básicamente un mensaje del paquete de seguridad asociado al cliente al paquete de seguridad asociado al servidor. Por lo tanto, la creación de un contexto de seguridad normalmente requiere que tanto el cliente como el servidor realicen llamadas a sus respectivos paquetes de seguridad. Para obtener más información sobre las funciones de contexto, vea [Context Management](authentication-functions.md).

El protocolo utilizado para establecer una conexión segura y autenticada implica el intercambio de uno o varios "tokens de seguridad" entre el cliente y el servidor. Estos tokens se envían como mensajes opacos por los dos lados junto con cualquier otra información específica [*del protocolo*](/windows/desktop/SecGloss/a-gly)de aplicación. Como mensaje opaco, el cliente recibe el token de una función de paquete de seguridad, que no puede interpretarlo ni cambiarlo, y lo reenvía como un mensaje al servidor. El token también es opaco para el servidor, que no puede interpretar ni cambiar el token. El servidor reenvía el token opaco a su paquete de seguridad para su interpretación. A continuación, el paquete informa al servidor de la autenticación del cliente o de un error al autenticarse.

El cliente recibe el token del servidor en un mensaje, recupera el token del mensaje recibido y usa ese token en una llamada a su paquete de seguridad. A continuación, el cliente llama de nuevo al paquete de seguridad para indicar si se ha establecido una conexión segura o si se necesitan más intercambios antes de que una conexión segura esté lista. En teoría, no hay ningún límite en el número de intercambios de tokens de seguridad necesarios. En la práctica, solo se requiere un número limitado de intercambios. La autenticación NTLM se basa en el esquema de desafío/respuesta y usa tres turnos para autenticar un cliente en el servidor. El [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) versión 5.0 puede requerir intercambios de mensajes adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de contexto de cliente](client-context-initialization.md)
</dt> <dt>

[Inicialización del contexto de servidor](server-context-initialization.md)
</dt> </dl>

 

 
