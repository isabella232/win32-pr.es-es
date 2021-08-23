---
title: Lista de escucha de IP
description: Las API de servidor HTTP no se enlazan a ninguna dirección IP y pares de puerto TCP hasta que un usuario registra un urlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dfc3f1763a9372911923cf24e50959bc6ac15e030c1b04daf3f81b45bff7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340525"
---
# <a name="ip-listen-list"></a>Lista de escucha de IP

Las API de servidor HTTP no se enlazan a ninguna dirección IP y pares de puerto TCP hasta que un usuario registra un urlPrefix. De forma predeterminada, una vez que se especifica un registro en la cola de solicitudes, la API del servidor HTTP se enlaza al puerto especificado en UrlPrefix (por ejemplo, el puerto 80) para todas las direcciones IP (INADDR ANY o \_ INADDR6 ANY) disponibles en \_ el equipo. Los problemas surgen cuando las aplicaciones de terceros (que no usan las API del servidor HTTP) se enlazan a pares de dirección IP y puerto 80 en la máquina. La API del servidor HTTP proporciona una manera de configurar la lista de direcciones IP que enlaza y resuelve este problema de coexistencia. El administrador del sistema llama a la [**función HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en el valor HttpServiceConfigIPListenList para especificar la lista de escucha de IP. Las direcciones IPv4 e IPv6 se pueden agregar a la lista. Las direcciones IP especificadas se aplican a todas las aplicaciones de la máquina mediante la API del servidor HTTP y se conservan en los reinicios de la máquina. Sin embargo, los cambios en la configuración de la lista de escuchas de IP no se llevan a cabo dinámicamente; en la mayoría de los casos, puede ser necesario reiniciar el sistema.

 

 




