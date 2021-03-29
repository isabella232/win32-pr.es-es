---
description: La autenticación inicial tiene lugar cuando el servidor recibe una respuesta de desafío de un cliente.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Autenticación inicial mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912478"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Autenticación inicial mediante Microsoft Digest

La autenticación inicial tiene lugar cuando el servidor recibe una respuesta de desafío de un cliente. La autenticación de una respuesta de desafío normalmente implica un mínimo de dos servidores:

-   El servidor de origen: recibe la solicitud del cliente y emite un desafío y, a continuación, recibe la respuesta de desafío del cliente que se debe autenticar.
-   El servidor de autenticación: recibe información de autorización del servidor de origen y realiza la autenticación. Este servidor suele ser un controlador de dominio que admite varios servidores de origen.

Cuando el servidor de origen recibe una solicitud con un encabezado de autorización que contiene una respuesta de desafío de síntesis, la autenticación continúa como sigue:

-   La identidad del servidor de origen se comprueba con respecto al servidor codificado en el nonce del desafío.
-   Se comprueba la marca de tiempo codificada en el nonce. Si el valor de seguridad (nonce) ha expirado y la información de nombre de usuario/contraseña es válida, el servidor de origen finaliza la autenticación emitiendo un nuevo desafío de síntesis con la Directiva obsoleta establecida en "true". Esto indica que solo el nonce estaba "obsoleto" y el cliente puede responder al nuevo desafío mediante la contraseña que usó en la respuesta anterior. Si el cliente recibe un nuevo desafío después de enviar la respuesta de desafío para el desafío obsoleto, el cliente debe generar una nueva respuesta de desafío.
-   Si se aplica la detección de la reproducción, se comprueba la Directiva de NC (recuento de nonce) con la base de datos de sesión de nonce mantenida por el servidor.
-   El servidor de autenticación se identifica y envía la información de autorización del cliente.
-   El servidor de autenticación comprueba la identidad del servidor codificado en el nonce con la identidad del servidor de origen.
-   El servidor de autenticación, que es un controlador de dominio, recupera la contraseña del usuario.
-   Con la información de autorización, la contraseña y la identificación del servidor de origen, el servidor de autenticación calcula el valor que el cliente debe haber proporcionado en la Directiva de respuesta de la respuesta de desafío. El servidor de autenticación compara el valor calculado con la respuesta del cliente para determinar si la autenticación se ha realizado correctamente o no.

Si la autenticación es correcta, el [*contexto de seguridad*](../secgloss/s-gly.md) del usuario y una [*clave de sesión*](../secgloss/s-gly.md) de resumen se devuelven al servidor de origen. Si se produce un error en la autenticación, el servidor de origen debe generar una respuesta de error. Después de una autenticación correcta, el servidor de origen devuelve el recurso solicitado al cliente.

La clave de sesión de Resumen devuelta por el servidor de autenticación se almacena en caché por el servidor de origen para su uso en la autenticación de solicitudes futuras. Para obtener más información, vea [autenticar solicitudes posteriores mediante Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
