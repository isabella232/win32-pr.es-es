---
description: En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan algo.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceptos básicos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155276"
---
# <a name="basic-authentication-concepts"></a>Conceptos básicos de autenticación

En un modelo de aplicación cliente/servidor, los clientes son programas que actúan en nombre de los usuarios que necesitan algo. Esto podría ser abrir y utilizar un archivo, tener acceso a un buzón, consultar una base de datos o imprimir un documento. Los servidores son programas que proporcionan servicios a clientes como almacenamiento de archivos, control de correo, procesamiento de consultas y puesta en cola de impresión. Los clientes inician la acción, los servidores responden. Normalmente, un servidor escucha en un puerto de comunicaciones en espera de que los clientes se conecten y soliciten el servicio.

En el modelo de protocolo Kerberos, cada conexión cliente/servidor comienza con la autenticación. El cliente y el servidor, sucesivamente, ejecutan una serie de acciones diseñadas para garantizar a cada una de las partes de la conexión que la otra es auténtica. Si la autenticación se lleva a cabo correctamente, la configuración de la sesión finalizará y se establecerá una sesión cliente/servidor segura.

El protocolo Kerberos hace uso de:

-   [Autenticación de clave](key-authentication.md)
-   [Mensajes del autenticador](authenticator-messages.md)
-   [Distribución de claves](key-distribution.md)
-   [Vales de sesión](session-tickets.md)
-   [Vales de concesión de vales](ticket-granting-tickets.md)

 

 



