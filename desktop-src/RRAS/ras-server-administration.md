---
title: Administración del servidor RAS
description: Windows NT Server 4.0 proporciona un conjunto de funciones para administrar los permisos de usuario y los puertos en Windows servidores RAS nt/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administración del servidor, RAS
- Administration, RAS Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6760e8cc06e5c7b389d01f690497dc070974cada5e9a922ec5576e48b2a328fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789194"
---
# <a name="ras-server-administration"></a>Administración del servidor RAS

Windows NT Server 4.0 proporciona un conjunto de funciones para administrar los permisos de usuario y los puertos en Windows servidores RAS nt/Windows 2000. Windows 95 no admite estas funciones. Con estas funciones, puede desarrollar una aplicación de administración de servidores RAS para realizar las siguientes tareas:

-   Enumerar los usuarios que tienen un conjunto especificado de permisos RAS
-   Asignación o revocación de permisos RAS para un usuario especificado
-   Enumerar los puertos configurados en un servidor RAS
-   Obtener información y estadísticas sobre un puerto especificado en un servidor RAS
-   Restablecer los contadores de estadísticas para un puerto especificado
-   Desconectar un puerto especificado

También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico. El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse.

 

 




