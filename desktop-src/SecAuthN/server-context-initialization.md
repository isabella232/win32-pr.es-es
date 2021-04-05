---
description: Al igual que el cliente, el servidor también adquiere un identificador de credenciales para estar listo para responder a una solicitud de autenticación entrante desde el cliente.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Inicialización de contexto de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813579"
---
# <a name="server-context-initialization"></a>Inicialización de contexto de servidor

Al igual que el cliente, el servidor también adquiere un identificador de [*credenciales*](../secgloss/c-gly.md) para estar listo para responder a una solicitud de autenticación entrante desde el cliente. Las credenciales del servidor se usan para autenticar el servidor en el cliente en [*protocolos de seguridad*](../secgloss/s-gly.md) que admiten la autenticación de servidor o la autenticación mutua. El servidor obtiene un identificador de sus credenciales definidas por la cuenta de servicio usada para iniciar el servidor. Para ello, llama a [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).

El servidor puede adquirir su identificador de credenciales y, a continuación, pasar a un estado de escucha, o puede esperar en un estado de escucha hasta que llegue una solicitud de conexión y, a continuación, adquiera un identificador de credenciales de entrada. Para obtener más información sobre las funciones de credenciales, vea [Administración de credenciales](authentication-functions.md).

Cuando el servidor recibe un mensaje de solicitud de conexión de un cliente, crea un [*contexto de seguridad*](../secgloss/s-gly.md) local para el cliente mediante [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext). El servidor utiliza este contexto de seguridad local para llevar a cabo solicitudes futuras del mismo cliente. Para obtener más información sobre las funciones de contexto, consulte [Administración de contexto](authentication-functions.md).

El servidor comprueba el estado de retorno y el descriptor de búfer de salida para asegurarse de que no hay errores hasta el momento y puede rechazar la solicitud de conexión si hay errores. Si hay información en el búfer de salida devuelto por [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), empaqueta ese búfer en un mensaje de respuesta al cliente.

Cualquier búfer de salida de [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) debe enviarse de vuelta al cliente. Además, si el estado de retorno requiere que el protocolo continúe (seg., es \_ \_ \_ necesario o \_ seg \_ \_ y \_ continuar), se requiere otro intercambio de mensajes con el cliente.

En el caso de las piernas adicionales, el servidor espera a que el cliente responda con otro mensaje. Este tiempo de espera se puede agotar para evitar un ataque de denegación de servicio en el que un cliente nunca responde de forma intencionada, lo que provoca que un subproceso de servidor y pronto, todos los subprocesos de servidor, deje de responder.

 

 
