---
title: Acerca de la administración del servicio de acceso remoto
description: Windows sistemas operativos 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos de usuario y los puertos en servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS, descrito
- RRAS de administración de RAS
- RRAS de administración de RAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67939d142763f45bc2eb52e959d8448904559c98357544c6c858b46e8f87a917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792288"
---
# <a name="about-remote-access-service-administration"></a>Acerca de la administración del servicio de acceso remoto

Windows sistemas operativos 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos de usuario y los puertos en servidores RAS. Con estas funciones, puede desarrollar una aplicación de administración de servidores RAS para realizar las siguientes tareas:

-   Enumerar los usuarios que tienen un conjunto especificado de permisos RAS
-   Asignación o revocación de permisos RAS para un usuario especificado
-   Enumerar los puertos configurados en un servidor RAS
-   Obtener información y estadísticas sobre un puerto especificado en un servidor RAS
-   Restablecer los contadores de estadísticas para un puerto especificado
-   Desconectar un puerto especificado

También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico. El archivo DLL exporta un conjunto de funciones a las que llama el servidor RAS cada vez que un usuario intenta conectarse o desconectarse.

En esta documentación se describen los temas siguientes:

-   [Comparación de funciones: Windows 2000 frente a RRAS Redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Administración de usuarios ras](ras-user-administration.md)
-   [Administración de puertos y servidores RAS](ras-server-and-port-administration.md)
-   [DLL de administración de RAS](ras-administration-dll.md)
-   [Instalación del Registro dll de administración de RAS](ras-administration-dll-registry-setup.md)

 

 




