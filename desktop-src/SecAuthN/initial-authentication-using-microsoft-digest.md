---
description: La autenticación inicial tiene lugar cuando el servidor recibe una respuesta de desafío de un cliente.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Autenticación inicial mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071296"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Autenticación inicial mediante Microsoft Digest

La autenticación inicial tiene lugar cuando el servidor recibe una respuesta de desafío de un cliente. La autenticación de una respuesta de desafío normalmente implica un mínimo de dos servidores:

-   El servidor de origen: recibe la solicitud del cliente y emite un desafío y, a continuación, recibe la respuesta del desafío del cliente que debe autenticarse.
-   Servidor de autenticación: recibe información de autorización del servidor de origen y realiza la autenticación. Este servidor suele ser un controlador de dominio que admite varios servidores de origen.

Cuando el servidor de origen recibe una solicitud con un encabezado de autorización que contiene una respuesta de desafío de resumen, la autenticación continúa de la siguiente manera:

-   La identidad del servidor de origen se comprueba con el servidor codificado en el valor nonce del desafío.
-   Se comprueba la marca de tiempo codificada en el valor nonce. Si el valor nonce ha expirado y la información de nombre de usuario o contraseña es válida, el servidor de origen finaliza la autenticación mediante la emisión de un nuevo desafío de resumen con la directiva obsoleta establecida en "true". Esto indica que solo el nonce era "obsoleto" y el cliente puede responder al nuevo desafío mediante la contraseña que usó en la respuesta anterior. Si el cliente recibe un nuevo desafío después de enviar la respuesta del desafío para el desafío obsoleto, el cliente debe generar una nueva respuesta de desafío.
-   Si se aplica la detección de reproducción, la directiva nc (número de nonce) se comprueba con la base de datos de sesión nonce mantenida por el servidor.
-   El servidor de autenticación se identifica y envía la información de autorización del cliente.
-   El servidor de autenticación comprueba la identidad del servidor codificado en nonce con la identidad del servidor de origen.
-   El servidor de autenticación, que es un controlador de dominio, recupera la contraseña del usuario.
-   Con la información de autorización, la contraseña y la identificación del servidor de origen, el servidor de autenticación calcula el valor que el cliente debe haber proporcionado en la directiva de respuesta de la respuesta de desafío. El servidor de autenticación compara el valor calculado con la respuesta del cliente para determinar el éxito o error de la autenticación.

Si la autenticación se realiza correctamente, el contexto [*de*](../secgloss/s-gly.md) seguridad del usuario y una clave de sesión [*implícita*](../secgloss/s-gly.md) se devuelven al servidor de origen. Si se produce un error en la autenticación, el servidor de origen debe generar una respuesta de error. Después de una autenticación correcta, el servidor de origen devuelve el recurso solicitado al cliente.

El servidor de origen almacena en caché la clave de sesión implícita devuelta por el servidor de autenticación para su uso en la autenticación de solicitudes futuras. Para obtener más información, vea [Authenticating Subsequent Requests using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
