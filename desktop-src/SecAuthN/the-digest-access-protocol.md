---
description: El protocolo de acceso de resumen
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: El protocolo de acceso de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160951"
---
# <a name="the-digest-access-protocol"></a>El protocolo de acceso de resumen

El protocolo de acceso implícita especificado por [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) se implementa mediante el proveedor de Microsoft Digest [*de*](../secgloss/s-gly.md) seguridad (SSP). La implementación consta de un conjunto de funciones de contexto de seguridad de la Interfaz de proveedor de compatibilidad de seguridad (SSPI) de [Microsoft](sspi.md) a las que llaman las aplicaciones cliente/servidor:

-   Establezca un contexto [*de seguridad para*](../secgloss/s-gly.md) el intercambio de mensajes.
-   Obtenga objetos de datos requeridos por el SSP de resumen, como credenciales [*y*](../secgloss/c-gly.md) identificadores de contexto.
-   Acceso a mecanismos [*de integridad*](../secgloss/i-gly.md) y confidencialidad de los mensajes.

La autenticación de acceso implícita tiene lugar dentro de transacciones de solicitud/respuesta emparejadas, con solicitudes originadas en el cliente y respuestas originadas en el servidor. Una autenticación de acceso implícita correcta requiere dos pares de solicitud/respuesta.

Cuando se usa el SSP de resumen para la autenticación HTTP, no se mantiene ninguna conexión entre el primer y el segundo par de solicitud y respuesta. En otras palabras, el servidor no espera a la segunda solicitud después de enviar la primera respuesta.

En la ilustración siguiente se muestran los pasos que un cliente y servidor han realizado en la ruta de acceso HTTP para completar una autenticación mediante el SSP de resumen. El mecanismo SASL hace uso de la autenticación mutua, por lo que los datos de autenticación se envían de vuelta en la llamada final del servidor de ASC al cliente que comprueba que el cliente se está comunicando con el servidor correcto.

![protocolo de acceso de resumen](images/digest1.png)

El proceso comienza con el cliente que solicita un recurso protegido por acceso desde el servidor mediante el envío de la solicitud HTTP 1.

El servidor recibe la solicitud HTTP 1 y determina que el recurso requiere información de autenticación que no se incluyó en la solicitud. El servidor genera un desafío para el cliente como se muestra a continuación:

1.  El servidor obtiene sus credenciales [*llamando*](../secgloss/c-gly.md) a la [**función AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)
2.  El servidor genera el desafío Digest llamando a [**la función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  El servidor envía un WWW-Authenticate como respuesta a la solicitud del cliente (que se muestra como respuesta HTTP 1). El encabezado contiene el desafío Digest y una directiva opaca que contiene una referencia a un contexto [*de seguridad parcial*](../secgloss/s-gly.md) establecido para el cliente. El encabezado se envía con un código de estado 401 que indica que la solicitud de cliente generó un error de acceso no autorizado. Para obtener más información sobre el desafío Digest, vea [Contenido de un desafío de resumen](contents-of-a-digest-challenge.md) y [Generación del desafío de síntesis](generating-the-digest-challenge.md).
4.  El cliente recibe la respuesta HTTP 1, extrae el desafío digest enviado por el servidor y genera una respuesta de desafío implícita como se muestra a continuación:
    1.  Las credenciales del usuario se obtienen llamando a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) o solicitando al usuario las credenciales de forma interactiva.
    2.  La información de desafío y credenciales se pasa a [**la función InitializeSecurityContext (General),**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) que genera la respuesta del desafío Digest.
5.  El cliente envía un encabezado authorization que contiene la respuesta de desafío al servidor (que se muestra como solicitud HTTP 2). Para obtener más información sobre la respuesta de desafío implícita, vea Contenido de una respuesta de desafío [de resumen](contents-of-a-digest-challenge-response.md) y [Generación de la respuesta del desafío de resumen](generating-the-digest-challenge-response.md).
6.  El servidor recibe la solicitud HTTP 2, extrae la respuesta de desafío enviada por el cliente y autentica la información mediante una llamada a la [**función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Para más información sobre el proceso de autenticación, consulte [Autenticación inicial mediante Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  El servidor devuelve la respuesta HTTP 2 al cliente como la segunda y última respuesta requerida por el protocolo de acceso implícita. Si la autenticación se realiza correctamente, esta respuesta contiene el recurso solicitado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenido de una respuesta de desafío de resumen](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
