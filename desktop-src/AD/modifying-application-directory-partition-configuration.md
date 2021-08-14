---
title: Modificar la configuración de particiones del directorio de la aplicación
description: Una partición de directorio de aplicación se puede modificar cambiando determinados atributos del objeto crossRef que representa la partición del directorio de aplicación.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modificación de la configuración de particiones del directorio de aplicaciones ad
- Application Directory Partitions AD , Modificar configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc378536a552bb7612877fc09913fdbad9daf507adbb34b5f53f8946c946e8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186320"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modificar la configuración de particiones del directorio de la aplicación

Una partición de directorio de aplicación se puede modificar cambiando determinados atributos del [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicación. Para buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa una partición de directorio de aplicación determinada, busque en el contenedor Particiones un objeto **crossRef** que tenga un valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición del directorio de la aplicación. A continuación, se puede usar el nombre distintivo del objeto **crossRef** para enlazar con el **objeto crossRef.**

En la tabla siguiente se enumeran los atributos [**del objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que se pueden modificar.

| Atributo                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Especifica el retraso, en segundos, después de un cambio de objeto de origen antes de que se notifique al primer asociado de replicación. Para obtener más información, vea [Replicación de particiones de directorio de aplicación.](application-directory-partition-replication.md)                                                                                                   |
| [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Especifica el retraso, en segundos, entre las notificaciones posteriores al segundo, el tercero, y así sucesivamente en los asociados de replicación. Para obtener más información, vea [Replicación de particiones de directorio de aplicación.](application-directory-partition-replication.md)                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica el dominio que usa el subsistema de seguridad para interpretar las referencias de dominio local en los [**atributos nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de objetos de esa partición de directorio de aplicación. Para obtener más información, vea [Seguridad de particiones de directorio de aplicaciones.](application-directory-partition-security.md) |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contiene el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para cada controlador de dominio que hospeda una réplica de la partición del directorio de la aplicación. Para obtener más información, vea Agregar o eliminar una réplica de partición de [directorio de aplicación.](adding-or-deleting-an-application-directory-partition-replica.md)            |



 

 

 