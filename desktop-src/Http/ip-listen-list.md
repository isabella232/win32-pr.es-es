---
title: Lista de escucha de IP
description: Las API de servidor HTTP no se enlazan a ninguna dirección IP ni a pares de puertos TCP hasta que un usuario registra un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994552"
---
# <a name="ip-listen-list"></a>Lista de escucha de IP

Las API de servidor HTTP no se enlazan a ninguna dirección IP ni a pares de puertos TCP hasta que un usuario registra un UrlPrefix. De forma predeterminada, una vez que se escribe un registro en la cola de solicitudes, la API del servidor HTTP enlaza con el puerto especificado en el UrlPrefix (por ejemplo, el puerto 80) para todas las direcciones IP (inaddress \_ any o INADDR6 \_ any) disponibles en la máquina. Los problemas surgen cuando las aplicaciones de terceros (que no usan las API de servidor HTTP) se enlazan a los pares de dirección IP y puerto 80 en la máquina. La API del servidor HTTP proporciona una manera de configurar la lista de direcciones IP que enlaza y resuelve este problema de coexistencia. El administrador del sistema llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en el valor HttpServiceConfigIPListenList para especificar la lista de escucha de IP. Las direcciones IPv4 e IPv6 se pueden agregar a la lista. Las direcciones IP especificadas se aplican a todas las aplicaciones del equipo mediante la API del servidor HTTP y se conservan a lo largo de los reinicios de la máquina. Sin embargo, los cambios en la configuración de la lista de escucha de IP no tienen lugar de forma dinámica. en la mayoría de los casos, es posible que sea necesario reiniciar el sistema.

 

 




