---
title: Modificar la configuración de la partición de directorio de aplicaciones
description: Una partición de directorio de aplicación se puede modificar cambiando ciertos atributos del objeto crossRef que representa la partición del directorio de aplicaciones.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modificar la configuración de la partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones AD, modificar configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c976c297e8491dbb87a32cf2241446ca0403e7f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904491"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modificar la configuración de la partición de directorio de aplicaciones

Una partición de directorio de aplicación se puede modificar cambiando ciertos atributos del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicaciones. Para buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa una partición de directorio de aplicación determinada, busque en el contenedor de particiones un objeto **crossRef** que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual al nombre distintivo de la partición de directorio de aplicaciones. A continuación, se puede utilizar el nombre distintivo del objeto **crossRef** para enlazar con el objeto **crossRef** .

En la tabla siguiente se enumeran los atributos del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que se puede modificar.

| Atributo                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Especifica el retraso, en segundos, después de que un objeto de origen cambie antes de que se notifique al primer asociado de replicación. Para obtener más información, consulte [replicación de particiones de directorio de aplicaciones](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-subsiguientes-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Especifica el retraso, en segundos, entre las siguientes notificaciones en el segundo, tercer y así sucesivamente los asociados de replicación. Para obtener más información, consulte [replicación de particiones de directorio de aplicaciones](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica el dominio que utiliza el subsistema de seguridad para interpretar las referencias de dominio local en los atributos [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de los objetos de esa partición de directorio de aplicaciones. Para obtener más información, consulte Seguridad de las [particiones de directorio de aplicaciones](application-directory-partition-security.md). |
| [**msDS-NC-réplica-ubicaciones**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contiene el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para cada controlador de dominio que hospeda una réplica de la partición de directorio de aplicaciones. Para obtener más información, vea [Agregar o eliminar una réplica de partición de directorio de aplicaciones](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 