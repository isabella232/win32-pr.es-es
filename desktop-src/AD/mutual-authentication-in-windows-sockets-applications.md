---
title: Autenticación mutua en aplicaciones de Windows Sockets
description: Los servicios de Microsoft Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios, o bien pueden usar puntos de conexión de servicio.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en aplicaciones de Windows Sockets
- Active Directory, uso, autenticación mutua, en aplicaciones de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268273"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Autenticación mutua en aplicaciones de Windows Sockets

Los servicios de Microsoft Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios, o bien pueden usar puntos de conexión de servicio.

Para obtener más información y un ejemplo de código que muestra cómo realizar la autenticación mutua para un servicio de Windows Sockets que se publica mediante un punto de conexión de servicio, consulte [autenticación mutua en un servicio de Windows Sockets con un SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). En este ejemplo de código se usa un paquete de seguridad de SSPI para administrar las negociaciones de autenticación entre un cliente y el servicio WinSock.

Un servicio WinSock RnR puede usar un código similar para realizar la autenticación mutua mediante un paquete SSPI. En este caso, el servicio crearía sus SPN con el nombre distintivo de la entrada del servicio en el contenedor WinsockServices del directorio.

Por ejemplo, si el servicio se registra a sí mismo con el nombre "WinSockRnRSampleService", crearía el SPN del servicio a partir del nombre distintivo siguiente:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




