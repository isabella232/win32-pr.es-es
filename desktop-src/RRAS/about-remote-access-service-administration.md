---
title: Acerca de la administración del servicio de acceso remoto
description: Los sistemas operativos Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS, descripción
- RRAS de administración de RAS
- RRAS de administración de RAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676173"
---
# <a name="about-remote-access-service-administration"></a>Acerca de la administración del servicio de acceso remoto

Los sistemas operativos Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS. Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS para realizar las siguientes tareas:

-   Enumerar a los usuarios que tienen un conjunto especificado de permisos de RAS
-   Asignar o revocar permisos RAS para un usuario especificado
-   Enumerar los puertos configurados en un servidor RAS
-   Obtener información y estadísticas acerca de un puerto específico en un servidor RAS
-   Restablecer los contadores de estadísticas de un puerto específico
-   Desconectar un puerto especificado

También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico. El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse.

En esta documentación se describen los temas siguientes:

-   [Comparación de funciones: Windows 2000 frente a RRAS Redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Administración de usuarios de RAS](ras-user-administration.md)
-   [Administración de puertos y servidores RAS](ras-server-and-port-administration.md)
-   [DLL de administración de RAS](ras-administration-dll.md)
-   [Configuración del registro del archivo DLL de administración de RAS](ras-administration-dll-registry-setup.md)

 

 




