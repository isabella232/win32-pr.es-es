---
description: Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, el lado cliente de Microsoft Digest almacena en caché la información recibida después de la autenticación correcta con un servidor.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Mantenimiento del contexto de seguridad entre conexiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361028"
---
# <a name="maintaining-the-security-context-between-connections"></a>Mantenimiento del contexto de seguridad entre conexiones

Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, el lado cliente de Microsoft Digest almacena en caché la información recibida después de la autenticación correcta con un servidor. Las aplicaciones cliente solo necesitan almacenar en caché el identificador del [*contexto de seguridad*](../secgloss/s-gly.md) que se ha establecido. En la tabla siguiente se describe la información almacenada en caché por el paquete de seguridad.



| Información                                                       | Descripción                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de servidor                                                       | El servidor que ha creado correctamente un contexto de seguridad para el usuario.                                                                           |
| Dominio Kerberos                                                      | El nombre de dominio usado en la autenticación correcta.                                                                                              |
| [*Emisor*](../secgloss/n-gly.md) | Un nonce de servidor que está asociado a la autenticación correcta.                                                                               |
| Recuento de nonce                                                       | El número de veces que el cliente ha incluido el valor de seguridad (nonce) en las solicitudes al servidor. Se utiliza para la detección de la reproducción.                                 |
| Valor opaco                                                      | El valor devuelto para la Directiva opaca después de una autenticación correcta. Este valor contiene una referencia al contexto de seguridad del usuario. |



 

Cuando un cliente envía un mensaje a un servidor, el servidor debe determinar si el cliente tiene un contexto de seguridad existente. Para ello, el servidor pasa cada solicitud de cliente a la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Esta función extrae el valor de la Directiva opaca de la solicitud, si está presente, y lo usa para buscar el contexto de seguridad del cliente. Si se encuentra el contexto de seguridad, el identificador del contexto se devuelve al servidor. Para obtener información relacionada, vea [autenticar solicitudes posteriores](authenticating-subsequent-requests-using-microsoft-digest.md).

Como medio para detectar ataques de suplantación de identidad y reproducción, el cliente llama a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) , que utiliza un contexto de seguridad para firmar un mensaje. Cuando los mensajes se protegen con la función **MakeSignature** , el servidor utiliza la función [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) con el contexto almacenado en caché para comprobar el origen y la [*integridad*](../secgloss/i-gly.md)del mensaje. Para obtener más información, consulte [protección de mensajes](protecting-messages-using-microsoft-digest.md).

 

 
