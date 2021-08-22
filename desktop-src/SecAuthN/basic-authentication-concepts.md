---
description: En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan hacer algo.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceptos básicos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d28aa1da3555561740dfd119603a42268ebf86056842788f7dbb1c473fe60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141318"
---
# <a name="basic-authentication-concepts"></a>Conceptos básicos de autenticación

En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan hacer algo. Esto podría ser abrir y usar un archivo, acceder a un buzón, consultar una base de datos o imprimir un documento. Los servidores son programas que proporcionan servicios a los clientes, como el almacenamiento de archivos, el control de correo, el procesamiento de consultas y la cola de impresión. Los clientes inician una acción y los servidores responden. Normalmente, un servidor escucha en un puerto de comunicaciones a la espera de que los clientes se conecten y soliciten el servicio.

En el modelo de protocolo Kerberos, cada conexión cliente/servidor comienza con la autenticación. El cliente y el servidor, sucesivamente, ejecutan una serie de acciones diseñadas para garantizar a cada una de las partes de la conexión que la otra es auténtica. Si la autenticación se lleva a cabo correctamente, la configuración de la sesión finalizará y se establecerá una sesión cliente/servidor segura.

El protocolo Kerberos usa:

-   [Autenticación de clave](key-authentication.md)
-   [Authenticator mensajes](authenticator-messages.md)
-   [Distribución de claves](key-distribution.md)
-   [Vales de sesión](session-tickets.md)
-   [Vales de concesión de vales](ticket-granting-tickets.md)

 

 



