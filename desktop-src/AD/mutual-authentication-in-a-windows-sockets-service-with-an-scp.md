---
title: Autenticación mutua en un servicio Windows sockets con SCP
description: Los temas de esta sección incluyen ejemplos de código que muestran cómo realizar la autenticación mutua con un servicio que se publica a sí mismo mediante un punto de conexión de servicio (SCP).
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en un servicio Windows Sockets con UN SCP AD
- Active Directory, mediante la autenticación mutua, Windows de sockets con un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8f3e65b044198c5ebf703b1c62ac03eb07a4d57b6bc5dcf7c5463247815f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025773"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Autenticación mutua en un servicio Windows sockets con SCP

Los temas de esta sección incluyen ejemplos de código que muestran cómo realizar la autenticación mutua con un servicio que se publica a sí mismo mediante un punto de conexión de servicio (SCP). Los ejemplos se basan en un servicio microsoft Windows Sockets que usa un paquete SSPI para controlar la negociación de autenticación mutua entre un cliente y el servicio. Use los procedimientos siguientes para implementar la autenticación mutua en este escenario.

**Para registrar SPN en un directorio cuando se instala un servicio**

1.  Llame a [**la función DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear nombres de entidad de seguridad de servicio (SPN) para el servicio.
2.  Llame a [**la función DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar los SPN en la cuenta de servicio o la cuenta de equipo en cuyo contexto se ejecutará el servicio. Este paso lo debe realizar un administrador de dominio; Una excepción es que un servicio que se ejecuta en la cuenta LocalSystem puede registrar su SPN con el formato " " en la cuenta de <service class> / <host> equipo del host de servicio.

**Para comprobar la configuración al iniciar el servicio**

-   Compruebe que los SPN adecuados están registrados en la cuenta con la que se ejecuta el servicio. Para obtener más información, vea [Tareas de mantenimiento de cuentas de inicio de sesión.](logon-account-maintenance-tasks.md)

**Para autenticar el servicio en el inicio del cliente**

1.  Recupere los datos de conexión del punto de conexión de servicio del servicio.
2.  Establezca una conexión con el servicio.
3.  Llame a [**la función DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN para el servicio. Cree el SPN a partir de la cadena de clase de servicio conocida y los datos recuperados del punto de conexión de servicio. Estos datos incluyen el nombre de host del servidor en el que se ejecuta el servicio. Tenga en cuenta que el nombre de host debe ser un nombre DNS.
4.  Use un paquete de seguridad SSPI para realizar la autenticación:
    1.  Llame a [**la función AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir las credenciales del cliente.
    2.  Pase las credenciales de cliente y el SPN a la [**función InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) para generar un blob de seguridad que se enviará al servicio para la autenticación. Establezca la **marca ISC \_ REQ \_ MUTUAL \_ AUTH para** solicitar la autenticación mutua.
    3.  Exchange blobs con el servicio hasta que se complete la autenticación.
5.  Compruebe la máscara de funcionalidades devueltas para la marca **\_ DE AUTENTICACIÓN \_ MUTUA \_ de ISC REQ** para comprobar que se realizó la autenticación mutua.
6.  Si la autenticación se ha realizado correctamente, intercamba el tráfico con el servicio autenticado. Use la firma digital para asegurarse de que los mensajes entre el cliente y el servicio no se han alterado. A menos que los requisitos de rendimiento sean graves, use el cifrado. Para obtener más información y un ejemplo de código que muestra cómo usar las funciones [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)y [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) en un paquete SSPI, vea [Ensuring Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Para autenticar el cliente por el servicio cuando se conecta un cliente**

1.  Cargue un paquete de seguridad SSPI que admita la autenticación mutua.
2.  Cuando un cliente se conecta, use el paquete de seguridad para realizar la autenticación:
    1.  Llame a [**la función AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) para adquirir las credenciales del servicio.
    2.  Pase las credenciales de servicio y el blob de seguridad recibidos del cliente a la función [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para generar un blob de seguridad para enviarlo de vuelta al cliente.
    3.  Exchange blobs con el cliente hasta que se complete la autenticación.
3.  Compruebe la máscara de funcionalidades devueltas para la marca **\_ ASC RET \_ MUTUAL \_ AUTH** para comprobar que se realizó la autenticación mutua.
4.  Si la autenticación se ha realizado correctamente, intercamba el tráfico con el cliente autenticado. Use la firma digital y el cifrado a menos que el rendimiento sea un problema.

Para obtener más información y un ejemplo de código para este escenario de autenticación mutua, vea:

-   [Cómo autentica un cliente un servicio de sockets de Windows basado en SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Crear y registrar SPN para un servicio de sockets de Windows basado en SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Cómo un servicio Windows sockets autentica un cliente](how-a-windows-sockets-service-authenticates-a-client.md)

Para más información, consulte:

-   [Publicación con puntos de conexión de servicio](publishing-with-service-connection-points.md)
-   [Documentación de SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Documentación de Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 