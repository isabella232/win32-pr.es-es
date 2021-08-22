---
description: Al igual que el cliente, el servidor también adquiere un identificador de credenciales para estar listo para responder a una solicitud de autenticación entrante del cliente.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Inicialización del contexto de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d4a81c8033dc6b5dda8baca9ee7dfcc87d2b14c1cd139ff4a7f8eda99603f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918334"
---
# <a name="server-context-initialization"></a>Inicialización del contexto de servidor

Al igual que el cliente, el servidor también adquiere un identificador [*de*](../secgloss/c-gly.md) credenciales para estar listo para responder a una solicitud de autenticación entrante del cliente. Las credenciales del servidor se usan para autenticar el servidor en el cliente en [*protocolos*](../secgloss/s-gly.md) de seguridad que admiten autenticación de servidor o autenticación mutua. El servidor obtiene un identificador de sus credenciales definidas por la cuenta de servicio utilizada para iniciar el servidor. Para ello, llama a [**AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)

El servidor puede adquirir su identificador de credenciales y, a continuación, pasar a un estado de escucha, o puede esperar en un estado de escucha hasta que llegue una solicitud de conexión y, a continuación, adquirir un identificador de credenciales de entrada. Para obtener más información sobre las funciones de credenciales, vea [Administración de credenciales.](authentication-functions.md)

Cuando el servidor recibe un mensaje de solicitud de conexión de un cliente, crea un contexto de seguridad [*local*](../secgloss/s-gly.md) para el cliente mediante [**AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) El servidor usa este contexto de seguridad local para llevar a cabo solicitudes futuras por parte del mismo cliente. Para obtener más información sobre las funciones de contexto, vea [Context Management](authentication-functions.md).

El servidor comprueba el estado de devolución y el descriptor del búfer de salida para asegurarse de que no hay errores hasta ahora y puede rechazar la solicitud de conexión si hay errores. Si hay información en el búfer de salida devuelto por [**AcceptSecurityContext (general),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)agrupa ese búfer en un mensaje de respuesta al cliente.

Cualquier búfer de salida [**de AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) debe devolverse al cliente. Además, si el estado de devolución requiere que el protocolo continúe (SEC I CONTINUE NEEDED o SEC I COMPLETE AND CONTINUE), se requiere otro intercambio \_ de mensajes con el \_ \_ \_ \_ \_ \_ cliente.

En el caso de las resas adicionales, el servidor espera a que el cliente responda con otro mensaje. Esta espera se puede tiempo de espera para evitar un ataque por denegación de servicio en el que un cliente nunca responde a propósito, lo que provoca que un subproceso de servidor y pronto, todos los subprocesos del servidor, dejen de responder.

 

 
