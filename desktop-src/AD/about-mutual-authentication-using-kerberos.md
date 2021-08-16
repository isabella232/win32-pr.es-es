---
title: Acerca de la autenticación mutua mediante Kerberos
description: En la autenticación mutua, el cliente y el servicio deben comprobar sus identidades respectivas entre sí antes de realizar funciones de aplicación.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Acerca de la autenticación mutua mediante Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b020b2d808cee96319cf411b4199bb4ff78f357cfdf8379f01c7d07bc1c5c1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841015"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Acerca de la autenticación mutua mediante Kerberos

En la autenticación mutua, el cliente y el servicio deben comprobar sus identidades respectivas entre sí antes de realizar funciones de aplicación. Ninguna parte puede realizar operaciones con la otra hasta que se haya comprobado la identidad; Es decir, el servicio debe ser capaz de comprobar el cliente sin consultar al cliente y el cliente debe poder comprobar el servicio sin consultar el servicio.

El valor de un servicio que puede autenticar un cliente es conocido. Por ejemplo, un servicio de archivos suplanta a un cliente para determinar a qué archivos puede acceder el cliente.

El valor de un cliente que puede autenticar un servicio es menos comprensible. La autenticación de un servicio permite al cliente confiar en los datos que obtiene del servicio y ser seguro al enviar datos confidenciales al servicio. La capacidad de un cliente para autenticar un servicio es especialmente importante en las aplicaciones cliente/servicio que admiten la delegación del contexto de seguridad del cliente. es decir, el cliente autoriza al servicio a actuar como delegado en el acceso a servicios adicionales o recursos de red.

Un servicio autentica un cliente de la siguiente manera: el cliente establece un contexto de seguridad local mediante la ejecución en un contexto establecido previamente, por ejemplo, en la sesión de un usuario que ha iniciado sesión o mediante la presentación explícita de credenciales al proveedor de seguridad subyacente. El servicio no puede aceptar conexiones de ningún cliente no autenticado.

El mecanismo kerberos mediante el que un cliente autentica un servicio funciona de la siguiente manera: cuando se instala un servicio, un instalador de servicio, que se ejecuta con privilegios de administrador, registra uno o varios SPN únicos para cada instancia de servicio. Los nombres se registran en Dominio de Active Directory Controller (DC) en el objeto de cuenta de usuario o equipo que usará la instancia de servicio para iniciar sesión. Cuando un cliente solicita una conexión a un servicio, crea un SPN para una instancia de servicio mediante datos conocidos proporcionados por el usuario. A continuación, el cliente usa el paquete de negociación de SSPI para presentar el SPN al Centro de distribución de claves (KDC) de la cuenta de dominio de cliente. El KDC busca en el bosque una cuenta de usuario o equipo en la que esté registrado ese SPN. Si el SPN está registrado en más de una cuenta, se produce un error en la autenticación. De lo contrario, el KDC cifra un mensaje con la contraseña de la cuenta en la que se registró el SPN. El KDC pasa este mensaje cifrado al cliente, que a su vez lo pasa a la instancia de servicio. El servicio usa el paquete de negociación de SSPI para descifrar el mensaje, que pasa de nuevo al cliente y al KDC del cliente. El KDC autentica el servicio si el mensaje descifrado coincide con su mensaje original.

-   Para obtener más información sobre la composición y el registro de SPN, vea . [Nombres de entidad de seguridad de servicio](service-principal-names.md)
-   Para obtener más información y un ejemplo de código que compone un SPN para un servicio Windows Sockets que se publica con un punto de conexión de servicio, vea Crear los SPN para un servicio con un [SCP.](composing-the-spns-for-a-service-with-an-scp.md)
-   Para obtener más información y un ejemplo de código que compone un SPN para un servicio RPC, vea Composición de [SPN para un servicio RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




