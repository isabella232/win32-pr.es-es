---
title: Autenticación mutua en Windows sockets
description: Los servicios Windows Sockets de Microsoft pueden usar las API de registro y resolución (RnR) para publicar servicios o pueden usar puntos de conexión de servicio.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en Windows sockets
- Active Directory, mediante, autenticación mutua, en aplicaciones Windows sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025753"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Autenticación mutua en Windows sockets

Los servicios Windows Sockets de Microsoft pueden usar las API de registro y resolución (RnR) para publicar servicios o pueden usar puntos de conexión de servicio.

Para obtener más información y un ejemplo de código que muestra cómo realizar la autenticación mutua para un servicio de sockets de Windows que publica mediante un punto de conexión de servicio, vea Autenticación mutua en un servicio [de sockets](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md)de Windows con un SCP . En este ejemplo de código se usa un paquete de seguridad SSPI para administrar las negociaciones de autenticación entre un cliente y el servicio WinSock.

Un servicio WinSock RnR puede usar código similar para realizar la autenticación mutua mediante un paquete SSPI. En este caso, el servicio crearía sus SPN con el nombre distintivo de la entrada del servicio en el contenedor WinsockServices del directorio .

Por ejemplo, si el servicio se registra con el nombre "WinSockRnRSampleService", crearía el SPN del servicio a partir del siguiente nombre distintivo:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




