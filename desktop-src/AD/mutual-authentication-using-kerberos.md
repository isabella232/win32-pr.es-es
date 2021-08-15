---
title: Autenticación mutua con Kerberos
description: La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente, antes de que se transmita cualquier tráfico de aplicación a través de la conexión de cliente o servicio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, mediante, autenticación mutua
- Active Directory, uso, seguridad, autenticación mutua
- seguridad de AD
- security AD, autenticación mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e22a9f83712b15f22f9d9b05aee4219f3cbc892d88d0b44ba2d63fb9bbe2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185955"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticación mutua con Kerberos

La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente, antes de que se transmita cualquier tráfico de aplicación a través de la conexión de cliente o servicio.

Active Directory Domain Services y Windows admiten nombres de entidad de seguridad de servicio (SPN), que son un componente clave en el mecanismo Kerberos mediante el cual un cliente autentica un servicio. Un SPN es un nombre único que identifica una instancia de un servicio y está asociado a la cuenta de inicio de sesión con la que se ejecuta la instancia de servicio. Los componentes de un SPN son tales que un cliente puede crear un SPN para un servicio sin la cuenta de inicio de sesión del servicio. Esto permite al cliente solicitar al servicio que autentique su cuenta aunque el cliente no tenga el nombre de cuenta.

En esta sección se incluye información general de:

-   Autenticación mutua mediante Kerberos.
-   Crear un SPN único.
-   Cómo un instalador de servicio registra SPN en el objeto de cuenta asociado a una instancia de servicio.
-   Cómo usa una aplicación cliente el objeto de punto de conexión de servicio (SCP) de una instancia de servicio en Active Directory Domain Services para recuperar los datos a partir de los cuales se va a crear un SPN para el servicio.
-   Cómo usa una aplicación cliente un SPN de servicio junto con la interfaz del proveedor de soporte técnico de seguridad (SSPI) para autenticar el servicio.
-   Un ejemplo de código para una Windows cliente o servicio de Sockets que usa un SCP y SSPI para realizar la autenticación mutua.
-   Un ejemplo de código para un cliente o servicio RPC que realiza la autenticación mutua mediante el servicio de nombres RPC y la autenticación RPC.
-   Cómo un Windows registro y resolución de sockets (RnR) usa SPN para realizar la autenticación mutua.

En esta sección se describe el uso de Dominio de Active Directory Service para la autenticación mutua, en particular, el propósito de los puntos de conexión de servicio y los nombres de entidad de seguridad de servicio en la autenticación mutua. No es una explicación completa de cómo usar SSPI para la autenticación mutua o la compatibilidad de autenticación y seguridad disponible para las aplicaciones RPC y Windows Sockets.

Para más información, consulte:

-   [Publicación con puntos de conexión de servicio](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 