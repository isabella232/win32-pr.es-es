---
title: Acerca de la administración del servicio de acceso remoto
description: Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos de usuario y los puertos en servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS, descrito
- RAS Administration RRAS
- RRAS de administración de RAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473625"
---
# <a name="about-remote-access-service-administration"></a>Acerca de la administración del servicio de acceso remoto

Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos de usuario y los puertos en servidores RAS. Con estas funciones, puede desarrollar una aplicación de administración de servidores RAS para realizar las siguientes tareas:

-   Enumerar los usuarios que tienen un conjunto especificado de permisos RAS
-   Asignación o revocación de permisos RAS para un usuario especificado
-   Enumerar los puertos configurados en un servidor RAS
-   Obtener información y estadísticas sobre un puerto especificado en un servidor RAS
-   Restablecer los contadores de estadísticas para un puerto especificado
-   Desconectar un puerto especificado

También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico. El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse.

En esta documentación se describen los temas siguientes:

-   [Comparación de funciones: Windows 2000 frente a RRAS Redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Administración de usuarios ras](ras-user-administration.md)
-   [Administración de puertos y servidores RAS](ras-server-and-port-administration.md)
-   [DLL de administración de RAS](ras-administration-dll.md)
-   [Instalación del Registro DLL de administración de RAS](ras-administration-dll-registry-setup.md)

 

 




