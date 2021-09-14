---
description: Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, el lado cliente de Microsoft Digest almacena en caché la información recibida después de la autenticación correcta con un servidor.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Mantener el contexto de seguridad entre conexiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173497"
---
# <a name="maintaining-the-security-context-between-connections"></a>Mantener el contexto de seguridad entre conexiones

Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, el lado cliente de Microsoft Digest almacena en caché la información recibida después de la autenticación correcta con un servidor. Las aplicaciones cliente solo necesitan almacenar en caché el identificador en el [*contexto de seguridad*](../secgloss/s-gly.md) que se ha establecido. En la tabla siguiente se describe la información almacenada en caché por el paquete de seguridad.



| Información                                                       | Descripción                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de servidor                                                       | Servidor que ha creado correctamente un contexto de seguridad para el usuario.                                                                           |
| Dominio o dominio                                                      | Nombre de dominio usado en la autenticación correcta.                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | Un valor nonce de servidor asociado a la autenticación correcta.                                                                               |
| Recuento de nonce                                                       | Número de veces que el cliente ha incluido el nonce en las solicitudes al servidor. Se usa para la detección de reproducción.                                 |
| Valor opaco                                                      | Valor devuelto para la directiva opaca después de una autenticación correcta. Este valor contiene una referencia al contexto de seguridad del usuario. |



 

Cuando un cliente envía un mensaje a un servidor, el servidor debe determinar si el cliente tiene un contexto de seguridad existente. Para ello, el servidor pasa cada solicitud de cliente a la [**función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Esta función extrae el valor de la directiva opaca de la solicitud, si está presente, y la usa para buscar el contexto de seguridad del cliente. Si se encuentra el contexto de seguridad, el identificador del contexto se devuelve al servidor. Para obtener información relacionada, vea [Authenticating Subsequent Requests](authenticating-subsequent-requests-using-microsoft-digest.md).

Como forma de detectar ataques de suplantación y reproducción, el cliente llama a la función [**MakeSignature,**](/windows/desktop/api/Sspi/nf-sspi-makesignature) que usa un contexto de seguridad para firmar un mensaje. Cuando los mensajes se protegen mediante la función **MakeSignature,** el servidor usa la función [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) con el contexto almacenado en caché para comprobar el origen y la integridad del [*mensaje.*](../secgloss/i-gly.md) Para obtener más información, vea [Protecting Messages](protecting-messages-using-microsoft-digest.md).

 

 
