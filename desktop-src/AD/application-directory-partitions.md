---
title: Particiones de directorio de aplicaciones
description: En Windows Server 2003, Active Directory Domain Services admiten particiones de directorio de aplicaciones.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- AD de particiones de directorio de aplicaciones
- Particiones de directorio de aplicaciones AD, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077567"
---
# <a name="application-directory-partitions"></a>Particiones de directorio de aplicaciones

En Windows Server 2003, Active Directory Domain Services admiten particiones de directorio de aplicaciones. Una partición de directorio de aplicaciones puede contener una jerarquía de cualquier tipo de objeto, excepto las entidades de seguridad, y se puede configurar para replicar en cualquier conjunto de controladores de dominio del bosque. A diferencia de una partición de dominio, no se necesita una partición de directorio de aplicaciones para replicar en todos los controladores de dominio de un dominio y la partición se puede replicar en controladores de dominio en dominios diferentes del bosque. Para obtener más información acerca de las particiones de directorio de aplicaciones, consulte [acerca de las particiones de directorio de aplicaciones](about-application-directory-partitions.md).

Se puede crear una partición de directorio de aplicaciones. se modificó y eliminó mediante las operaciones estándar ADSI, LDAP y [System. DirectoryServices](/dotnet/api/system.directoryservices) . El contexto de seguridad necesario para crear y modificar una partición de directorio de aplicación es el mismo que para crear una partición de dominio.

En los temas siguientes se describe cómo trabajar con particiones de directorio de aplicaciones:

-   [Replicación de partición de directorio de aplicaciones](application-directory-partition-replication.md)
-   [Seguridad de partición de directorio de aplicaciones](application-directory-partition-security.md)
-   [Crear una partición de directorio de aplicaciones](creating-an-application-directory-partition.md)
-   [Eliminar una partición de directorio de aplicaciones](deleting-an-application-directory-partition.md)
-   [Enumerar particiones de directorio de aplicaciones en un bosque](enumerating-application-directory-partitions-in-a-forest.md)
-   [Localizar un servidor host de partición de directorio de aplicaciones](locating-an-application-directory-partition-host-server.md)
-   [Agregar o eliminar una réplica de partición de directorio de aplicaciones](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Enumerar réplicas de una partición de directorio de aplicaciones](enumerating-replicas-of-an-application-directory-partition.md)
-   [Modificar la configuración de la partición de directorio de aplicaciones](modifying-application-directory-partition-configuration.md)

 

 