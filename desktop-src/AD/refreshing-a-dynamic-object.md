---
title: Actualizar un objeto dinámico
description: Un cliente puede actualizar el período de vida (TTL) de una entrada de directorio determinada para mantenerla activa en una de las dos formas de realizar una actualización LDAP en el valor de su atributo entryTTL antes de que la entrada se recopile como elemento no utilizado.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105656445"
---
# <a name="refreshing-a-dynamic-object"></a>Actualizar un objeto dinámico

Un cliente puede actualizar el período de vida (TTL) de una entrada de directorio determinada para mantenerla activo de una de estas dos maneras:

-   Realización de una actualización LDAP en el valor de su atributo **entryTTL** antes de que la entrada se recopile como elemento no utilizado. Este método de actualización de una entrada dinámica en el directorio es una característica adicional (opcional) de Active Directory Domain Services que no se especifica en RFC 2589.
-   Realización de una operación extendida de LDAP con un OID de 1.3.6.1.4.1.1466.101.119.1 para la actualización de TTL, como se estipula en RFC 2589. Este OID se define como **el \_ \_ OID de \_ OP \_ extendido de TTL de LDAP** en WINLDAP. H.

 
* * Comentario * * *: el recolector de elementos no utilizados quita los objetos dinámicos cuando han expirado, no hay ninguna fase del objeto que sea un objeto de desecho cuando haya expirado. Debe tener cuidado con la latencia de replicación de AD al actualizar los objetos. Debe asegurarse de que la actualización para actualizar el TTL llega lo suficientemente pronto como para que todas las réplicas del contexto de nomenclatura (catálogo global y completo) vean la transacción de actualización antes de que el objeto expire localmente.

 




