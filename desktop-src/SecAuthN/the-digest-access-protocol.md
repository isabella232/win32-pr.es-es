---
description: El protocolo de acceso implícita
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: El protocolo de acceso implícita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560253"
---
# <a name="the-digest-access-protocol"></a>El protocolo de acceso implícita

El [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) de Microsoft Digest implementa el protocolo de acceso implícita especificado por [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) . La implementación de consta de un conjunto de funciones de contexto de seguridad de la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI) de Microsoft a las que llaman las aplicaciones cliente/servidor:

-   Establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes.
-   Obtener objetos de datos requeridos por el SSP de síntesis, como [*credenciales*](../secgloss/c-gly.md) e identificadores de contexto.
-   Mecanismos de confidencialidad y [*integridad*](../secgloss/i-gly.md) del mensaje de acceso.

La autenticación de acceso implícita tiene lugar dentro de las transacciones de solicitud/respuesta emparejadas, con las solicitudes que se originan en el cliente y las respuestas que se originan en el servidor. Una autenticación de acceso implícita correcta requiere dos pares de solicitud/respuesta.

Cuando el SSP de síntesis se utiliza para la autenticación HTTP, no se mantiene ninguna conexión entre el primer y el segundo par de solicitud-respuesta. En otras palabras, el servidor no espera la segunda solicitud después de enviar la primera respuesta.

En la siguiente ilustración se muestran los pasos realizados en la ruta de acceso HTTP por un cliente y un servidor para completar una autenticación mediante el SSP de síntesis. El mecanismo SASL hace uso de la autenticación mutua, por lo que los datos de autenticación se devuelven en la llamada final de ASC Server al cliente que comprueba que el cliente se comunica con el servidor correcto.

![Protocolo de acceso implícita](images/digest1.png)

El proceso se inicia con el cliente que solicita un recurso protegido de acceso desde el servidor mediante el envío de la solicitud HTTP 1.

El servidor recibe la solicitud HTTP 1 y determina que el recurso requiere información de autenticación que no se incluyó en la solicitud. El servidor genera un desafío para el cliente de la manera siguiente:

1.  El servidor obtiene sus [*credenciales*](../secgloss/c-gly.md) mediante una llamada a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .
2.  El servidor genera el desafío de síntesis mediante una llamada a la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
3.  El servidor envía un encabezado WWW-Authenticate como respuesta a la solicitud del cliente (se muestra como respuesta HTTP 1). El encabezado contiene el desafío de síntesis y una directiva opaca que contiene una referencia a un [*contexto de seguridad*](../secgloss/s-gly.md) parcial establecido para el cliente. El encabezado se envía con un código de estado 401 que indica que la solicitud de cliente ha generado un error de acceso no autorizado. Para obtener más información sobre el desafío de síntesis, consulte [contenido de un desafío de síntesis](contents-of-a-digest-challenge.md) y [generación del desafío de síntesis](generating-the-digest-challenge.md).
4.  El cliente recibe la respuesta HTTP 1, extrae el desafío de síntesis enviado por el servidor y genera una respuesta de desafío de síntesis como se indica a continuación:
    1.  Las credenciales del usuario se obtienen mediante una llamada a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) o mediante la solicitud interactiva del usuario de las credenciales.
    2.  La información sobre el desafío y las credenciales se pasa a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , que genera la respuesta del desafío de síntesis.
5.  El cliente envía un encabezado de autorización que contiene la respuesta de desafío al servidor (que se muestra como solicitud HTTP 2). Para obtener más información acerca de la respuesta de desafío de síntesis, consulte [contenido de una respuesta de desafío de síntesis](contents-of-a-digest-challenge-response.md) y [generación de la respuesta de desafío de síntesis](generating-the-digest-challenge-response.md).
6.  El servidor recibe la solicitud HTTP 2, extrae la respuesta de desafío enviada por el cliente y autentica la información mediante una llamada a la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Para obtener más información sobre el proceso de autenticación, vea [autenticación inicial mediante Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  El servidor envía la respuesta HTTP 2 al cliente como la segunda y última respuesta requerida por el protocolo de acceso implícita. Si la autenticación es correcta, esta respuesta contiene el recurso solicitado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenido de una respuesta de desafío de síntesis](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
