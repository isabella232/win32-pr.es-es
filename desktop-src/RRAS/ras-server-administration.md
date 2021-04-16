---
title: Administración del servidor RAS
description: Windows NT Server 4,0 proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en servidores RAS de Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administración del servidor, RAS
- Administración, servidor RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269225"
---
# <a name="ras-server-administration"></a>Administración del servidor RAS

Windows NT Server 4,0 proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en servidores RAS de Windows NT/Windows 2000. Windows 95 no admite estas funciones. Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS para realizar las siguientes tareas:

-   Enumerar a los usuarios que tienen un conjunto especificado de permisos de RAS
-   Asignar o revocar permisos RAS para un usuario especificado
-   Enumerar los puertos configurados en un servidor RAS
-   Obtener información y estadísticas acerca de un puerto específico en un servidor RAS
-   Restablecer los contadores de estadísticas de un puerto específico
-   Desconectar un puerto especificado

También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico. El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse.

 

 




