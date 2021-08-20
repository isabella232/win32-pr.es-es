---
title: Particiones de directorio de aplicación
description: En Windows Server 2003, Active Directory Domain Services particiones de directorio de aplicaciones.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Ad de particiones de directorio de aplicación
- Application Directory Partitions AD , Using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d90532c813dde406fae3104b56ab2e68065145cf893b145f6148f39e6c1007e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024256"
---
# <a name="application-directory-partitions"></a>Particiones de directorio de aplicación

En Windows Server 2003, Active Directory Domain Services particiones de directorio de aplicaciones. Una partición de directorio de aplicación puede contener una jerarquía de cualquier tipo de objetos, excepto las entidades de seguridad, y se puede configurar para replicar en cualquier conjunto de controladores de dominio del bosque. A diferencia de una partición de dominio, no es necesaria una partición de directorio de aplicación para replicar en todos los controladores de dominio de un dominio y la partición se puede replicar en controladores de dominio de dominios diferentes del bosque. Para obtener más información sobre las particiones de directorio de aplicación, vea [Acerca de las particiones de directorio de aplicación.](about-application-directory-partitions.md)

Se puede crear una partición de directorio de aplicación. modificado y eliminado mediante las operaciones ADSI, LDAP y [System.DirectoryServices](/dotnet/api/system.directoryservices) estándar. El contexto de seguridad necesario para crear y modificar una partición de directorio de aplicación es el mismo que para crear una partición de dominio.

En los temas siguientes se describe cómo trabajar con particiones de directorio de aplicación:

-   [Replicación de particiones de directorio de aplicación](application-directory-partition-replication.md)
-   [Seguridad de la partición del directorio de la aplicación](application-directory-partition-security.md)
-   [Creación de una partición de directorio de aplicación](creating-an-application-directory-partition.md)
-   [Eliminación de una partición de directorio de aplicación](deleting-an-application-directory-partition.md)
-   [Enumeración de particiones de directorio de aplicación en un bosque](enumerating-application-directory-partitions-in-a-forest.md)
-   [Buscar un servidor host de partición de directorio de aplicación](locating-an-application-directory-partition-host-server.md)
-   [Agregar o eliminar una réplica de partición de directorio de aplicación](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Enumeración de réplicas de una partición de directorio de aplicación](enumerating-replicas-of-an-application-directory-partition.md)
-   [Modificar la configuración de particiones del directorio de la aplicación](modifying-application-directory-partition-configuration.md)

 

 