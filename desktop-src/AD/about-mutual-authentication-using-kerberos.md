---
title: Acerca de la autenticación mutua con Kerberos
description: En la autenticación mutua, el cliente y el servicio deben comprobar sus identidades respectivas entre sí antes de realizar las funciones de la aplicación.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Acerca de la autenticación mutua mediante Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075027"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Acerca de la autenticación mutua con Kerberos

En la autenticación mutua, el cliente y el servicio deben comprobar sus identidades respectivas entre sí antes de realizar las funciones de la aplicación. Ninguna de las partes puede realizar operaciones con la otra hasta que se haya comprobado la identidad; es decir, el servicio debe ser capaz de comprobar el cliente sin consultar al cliente y el cliente debe ser capaz de comprobar el servicio sin consultar el servicio.

El valor de un servicio que puede autenticar a un cliente es conocido. Por ejemplo, un servicio de archivo suplanta a un cliente para determinar a qué archivos puede tener acceso el cliente.

El valor de un cliente que puede autenticar un servicio es menos comprensible. La autenticación de un servicio permite que el cliente confíe en los datos que obtiene del servicio y que sea seguro para enviar datos confidenciales al servicio. La capacidad de un cliente para autenticar un servicio es especialmente importante en las aplicaciones de cliente/servicio que admiten la delegación del contexto de seguridad del cliente. es decir, el cliente autoriza el servicio para que actúe como su delegado en el acceso a servicios adicionales o recursos de red.

Un servicio autentica un cliente de la siguiente manera: el cliente establece un contexto de seguridad local mediante la ejecución en un contexto establecido previamente, por ejemplo, en la sesión de un usuario que ha iniciado sesión o mediante la presentación explícita de credenciales al proveedor de seguridad subyacente. El servicio no puede aceptar conexiones de ningún cliente no autenticado.

El mecanismo de Kerberos por el que un cliente autentica un servicio funciona de la siguiente manera: cuando se instala un servicio, un instalador de servicio que se ejecuta con privilegios de administrador, registra uno o más SPN únicos para cada instancia de servicio. Los nombres se registran en el controlador de Dominio de Active Directory (DC) del objeto de cuenta de usuario o de equipo que la instancia de servicio utilizará para iniciar sesión. Cuando un cliente solicita una conexión a un servicio, crea un SPN para una instancia de servicio con datos conocidos o datos proporcionados por el usuario. Después, el cliente utiliza el paquete de negociación de SSPI para presentar el SPN al Centro de distribución de claves (KDC) para la cuenta de dominio del cliente. El KDC busca en el bosque una cuenta de usuario o de equipo en la que se haya registrado el SPN. Si el SPN está registrado en más de una cuenta, se produce un error en la autenticación. De lo contrario, el KDC cifra un mensaje con la contraseña de la cuenta en la que se registró el SPN. El KDC pasa este mensaje cifrado al cliente, que a su vez lo pasa a la instancia de servicio. El servicio utiliza el paquete de negociación SSPI para descifrar el mensaje, que se devuelve al cliente y al KDC del cliente. El KDC autentica el servicio si el mensaje descifrado coincide con su mensaje original.

-   Para obtener más información acerca de la creación y el registro de SPN, vea. [Nombres de entidad](service-principal-names.md) de seguridad de servicio
-   Para obtener más información y un ejemplo de código que crea un SPN para un servicio de Windows Sockets que se publica con un punto de conexión de servicio, consulte [creación de SPN para un servicio con un SCP](composing-the-spns-for-a-service-with-an-scp.md).
-   Para obtener más información y un ejemplo de código que compone un SPN para un servicio RPC, consulte [composición de SPN para un servicio RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




