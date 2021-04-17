---
title: Autenticación mutua con Kerberos
description: La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente antes de que se transmita el tráfico de la aplicación a través de la conexión del cliente o servicio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, autenticación mutua
- Active Directory, uso, seguridad, autenticación mutua
- seguridad AD
- seguridad AD, autenticación mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656331"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticación mutua con Kerberos

La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente antes de que se transmita el tráfico de la aplicación a través de la conexión del cliente o servicio.

Active Directory Domain Services y Windows proporcionan compatibilidad con los nombres principales de servicio (SPN), que son un componente clave en el mecanismo de Kerberos mediante el cual un cliente autentica un servicio. Un SPN es un nombre único que identifica una instancia de un servicio y está asociado a la cuenta de inicio de sesión en la que se ejecuta la instancia de servicio. Los componentes de un SPN son de tal forma que un cliente puede crear un SPN para un servicio sin la cuenta de inicio de sesión del servicio. Esto permite al cliente solicitar al servicio que autentique su cuenta, aunque el cliente no tenga el nombre de la cuenta.

En esta sección se incluye información general sobre:

-   Autenticación mutua mediante Kerberos.
-   Crear un SPN único.
-   Cómo registra un instalador de servicio los SPN en el objeto de cuenta asociado a una instancia de servicio.
-   Cómo una aplicación cliente usa el objeto de punto de conexión de servicio (SCP) de una instancia de servicio en Active Directory Domain Services para recuperar datos de los que se va a crear un SPN para el servicio.
-   Cómo una aplicación cliente usa un SPN de servicio junto con la interfaz del proveedor de compatibilidad para seguridad (SSPI) para autenticar el servicio.
-   Un ejemplo de código para una aplicación de cliente o servicio de Windows Sockets que usa un SCP y SSPI para realizar la autenticación mutua.
-   Un ejemplo de código para un cliente o servicio RPC que realiza la autenticación mutua mediante el servicio de nombres RPC y la autenticación RPC.
-   Cómo un servicio de registro y resolución de Windows Sockets (RnR) usa SPN para realizar la autenticación mutua.

En esta sección se describe el uso de Dominio de Active Directory servicio para la autenticación mutua, en particular, el propósito de los puntos de conexión de servicio y los nombres de entidad de seguridad de servicio en la autenticación mutua. No es un debate completo sobre cómo usar SSPI para la autenticación mutua o la compatibilidad de autenticación y seguridad disponible para las aplicaciones RPC y Windows Sockets.

Para más información, consulte:

-   [Publicar con puntos de conexión de servicio](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 