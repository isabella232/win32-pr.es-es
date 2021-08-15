---
title: Actualizar un objeto dinámico
description: Un cliente puede actualizar el período de vida (TTL) de una entrada de directorio determinada para mantenerla activa de una de las dos maneras en que se realiza una actualización LDAP al valor de su atributo entryTTL antes de que la entrada se recolecte como elemento no utilizados.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025192"
---
# <a name="refreshing-a-dynamic-object"></a>Actualizar un objeto dinámico

Un cliente puede actualizar el período de vida (TTL) de una entrada de directorio determinada para mantenerlo activo de una de estas dos maneras:

-   Realizar una actualización LDAP al valor de su **atributo entryTTL** antes de que la entrada se recolecte como elemento no utilizados. Este método para actualizar una entrada dinámica en el directorio es una característica adicional (opcional) de Active Directory Domain Services que rfc 2589 no especifica.
-   Realizar una operación extendida ldap con un OID de 1.3.6.1.4.1.1466.101.119.1 para la actualización de TTL, como se indica en RFC 2589. Este OID se define como **\_ \_ \_ \_ OID de LDAP TTL EXTENDED OP** en WINLDAP.H.

 
**Comentario:: el recolector de elementos no utilizados quita los objetos dinámicos cuando han expirado, no hay ninguna fase en la que el objeto sea un lápido cuando ha expirado. Debe tener cuidado con la latencia de replicación de AD al actualizar objetos. Debe asegurarse de que la actualización para actualizar el TTL llega lo suficientemente pronto como para que todas las réplicas del contexto de nomenclatura (catálogo completo y global) vean la transacción de actualización antes de que el objeto expire localmente.

 




