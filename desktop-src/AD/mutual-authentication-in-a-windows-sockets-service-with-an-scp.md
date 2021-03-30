---
title: Autenticación mutua en un servicio de Windows Sockets con SCP
description: En los temas de esta sección se incluyen ejemplos de código que muestran cómo realizar la autenticación mutua con un servicio que se publica mediante un punto de conexión de servicio (SCP).
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en un servicio de Windows Sockets con un AD de SCP
- Active Directory, uso, autenticación mutua, servicio de Windows Sockets con un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904488"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Autenticación mutua en un servicio de Windows Sockets con SCP

En los temas de esta sección se incluyen ejemplos de código que muestran cómo realizar la autenticación mutua con un servicio que se publica mediante un punto de conexión de servicio (SCP). Los ejemplos se basan en un servicio de Microsoft Windows Sockets que usa un paquete SSPI para controlar la negociación de la autenticación mutua entre un cliente y el servicio. Utilice los procedimientos siguientes para implementar la autenticación mutua en este escenario.

**Para registrar los SPN en un directorio cuando se instala un servicio**

1.  Llame a la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear nombres de entidad de seguridad de servicio (SPN) para el servicio.
2.  Llame a la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar los SPN en la cuenta de servicio o la cuenta de equipo en cuyo contexto se ejecutará el servicio. Este paso lo debe realizar un administrador de dominio; una excepción es que un servicio que se ejecuta con la cuenta LocalSystem puede registrar su SPN con el formato " <service class> / <host> " en la cuenta de equipo del host del servicio.

**Para comprobar la configuración en el inicio del servicio**

-   Compruebe que los SPN adecuados están registrados en la cuenta en la que se está ejecutando el servicio. Para obtener más información, consulte tareas de mantenimiento de la [cuenta de inicio de sesión](logon-account-maintenance-tasks.md).

**Para autenticar el servicio en el inicio del cliente**

1.  Recuperar datos de conexión desde el punto de conexión de servicio del servicio.
2.  Establezca una conexión con el servicio.
3.  Llame a la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN para el servicio. Cree el SPN a partir de la cadena de clase de servicio conocida y los datos recuperados del punto de conexión de servicio. Estos datos incluyen el nombre de host del servidor en el que se ejecuta el servicio. Tenga en cuenta que el nombre de host debe ser un nombre DNS.
4.  Use un paquete de seguridad de SSPI para realizar la autenticación:
    1.  Llame a la función [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir las credenciales del cliente.
    2.  Pase las credenciales de cliente y el SPN a la función [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) para generar un BLOB de seguridad que se enviará al servicio para la autenticación. Establezca la marca **ISC \_ req \_ Mutual \_ auth** para solicitar autenticación mutua.
    3.  Intercambie blobs con el servicio hasta que se complete la autenticación.
5.  Compruebe la máscara de funcionalidades devueltas para la marca de autenticación mutua de REQ de ISC para comprobar que se realizó la autenticación mutua. **\_ \_ \_**
6.  Si la autenticación se realizó correctamente, intercambie el tráfico con el servicio autenticado. Use la firma digital para asegurarse de que los mensajes entre el cliente y el servicio no se han alterado. A menos que los requisitos de rendimiento sean graves, use el cifrado. Para obtener más información y un ejemplo de código que muestra cómo usar las funciones [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)y [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) en un paquete SSPI, consulte [garantizar la integridad de la comunicación durante el intercambio de mensajes](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Para autenticar el cliente por el servicio cuando un cliente se conecta**

1.  Cargue un paquete de seguridad de SSPI que admita la autenticación mutua.
2.  Cuando se conecte un cliente, use el paquete de seguridad para realizar la autenticación:
    1.  Llame a la función [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir las credenciales del servicio.
    2.  Pase las credenciales de servicio y el BLOB de seguridad recibido del cliente a la función [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para generar un BLOB de seguridad que se devolverá al cliente.
    3.  Intercambie blobs con el cliente hasta que se complete la autenticación.
3.  Compruebe la máscara de funcionalidades devueltas para la marca de autenticación **\_ \_ mutua \_ de ASC RET** para comprobar que se realizó la autenticación mutua.
4.  Si la autenticación se realizó correctamente, intercambie el tráfico con el cliente autenticado. Utilice la firma digital y el cifrado a menos que el rendimiento sea un problema.

Para obtener más información y un ejemplo de código para este escenario de autenticación mutua, vea:

-   [Cómo un cliente autentica un servicio de Windows Sockets basado en SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Creación y registro de SPN para un servicio de Windows Sockets basado en SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Cómo autentica un servicio de Windows Sockets un cliente](how-a-windows-sockets-service-authenticates-a-client.md)

Para más información, consulte:

-   [Publicar con puntos de conexión de servicio](publishing-with-service-connection-points.md)
-   [Documentación de SSPI](/windows/desktop/SecAuthN/sspi)
-   [Documentación de Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 