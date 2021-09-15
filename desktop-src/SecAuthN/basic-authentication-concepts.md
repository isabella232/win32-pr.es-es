---
description: En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan hacer algo.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceptos básicos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476563"
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

 

 



