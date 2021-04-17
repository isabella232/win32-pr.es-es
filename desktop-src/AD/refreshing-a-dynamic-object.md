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
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="c71cf-103">Actualizar un objeto dinámico</span><span class="sxs-lookup"><span data-stu-id="c71cf-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="c71cf-104">Un cliente puede actualizar el período de vida (TTL) de una entrada de directorio determinada para mantenerla activo de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="c71cf-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="c71cf-105">Realización de una actualización LDAP en el valor de su atributo **entryTTL** antes de que la entrada se recopile como elemento no utilizado.</span><span class="sxs-lookup"><span data-stu-id="c71cf-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="c71cf-106">Este método de actualización de una entrada dinámica en el directorio es una característica adicional (opcional) de Active Directory Domain Services que no se especifica en RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="c71cf-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="c71cf-107">Realización de una operación extendida de LDAP con un OID de 1.3.6.1.4.1.1466.101.119.1 para la actualización de TTL, como se estipula en RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="c71cf-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="c71cf-108">Este OID se define como **el \_ \_ OID de \_ OP \_ extendido de TTL de LDAP** en WINLDAP. H.</span><span class="sxs-lookup"><span data-stu-id="c71cf-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="c71cf-109">\* \* Comentario \* \* \*: el recolector de elementos no utilizados quita los objetos dinámicos cuando han expirado, no hay ninguna fase del objeto que sea un objeto de desecho cuando haya expirado.</span><span class="sxs-lookup"><span data-stu-id="c71cf-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="c71cf-110">Debe tener cuidado con la latencia de replicación de AD al actualizar los objetos.</span><span class="sxs-lookup"><span data-stu-id="c71cf-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="c71cf-111">Debe asegurarse de que la actualización para actualizar el TTL llega lo suficientemente pronto como para que todas las réplicas del contexto de nomenclatura (catálogo global y completo) vean la transacción de actualización antes de que el objeto expire localmente.</span><span class="sxs-lookup"><span data-stu-id="c71cf-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




