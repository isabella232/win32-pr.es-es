---
title: Objetos dinámicos
description: En Windows Server 2003 y versiones posteriores de Windows, Active Directory Domain Services proporcionan compatibilidad para almacenar entradas dinámicas en el directorio.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- AD de objetos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d521dabda8f82cbdcd46c00b3041f150f390d60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773243"
---
# <a name="dynamic-objects"></a>Objetos dinámicos

En Windows Server 2003 y versiones posteriores de Windows, Active Directory Domain Services proporcionan compatibilidad para almacenar entradas dinámicas en el directorio. Una entrada dinámica es un objeto del directorio que tiene un valor de período de vida (TTL) asociado. El TTL de una entrada se establece cuando se crea la entrada. El período de vida se reduce automáticamente y, cuando expira, desaparece la entrada dinámica. El cliente puede hacer que una entrada dinámica siga siendo más larga que su vida restante actual actualizando (modificando) su valor de TTL. Los clientes que almacenan datos dinámicos en el directorio deben actualizar periódicamente los datos para evitar que se desaparezcan.

Muchas aplicaciones y servicios que usan LDAP para almacenar y obtener acceso a datos relativamente estáticos y globales interesantes de un servidor de Active Directory preferirían seguir usando el acceso LDAP para sus necesidades de datos dinámicos. Además, en el caso de algunas aplicaciones, puede ser conveniente descargar la tarea de los objetos de recolección de elementos no utilizados en el DS que tienen una vida útil limitada al servicio de directorio. Las particiones de directorio de aplicaciones (con la capacidad de la ubicación controlada de réplicas) y el TTLs por objeto juntas proporcionarán la capacidad de hospedar datos dinámicos en Active Directory Domain Services, lo que permite el acceso LDAP a él.

Se definirá una nueva clase de objeto auxiliar denominada **dynamicObject** con OID = 1.3.6.1.4.1.1466.101.119.2 en el esquema de ad base que usarán las entradas dinámicas. Esta clase auxiliar contiene el atributo denominado **entryTTL** con OID = 1.3.6.1.4.1.1466.101.119.3 como atributo de inclusión del sistema. El valor de este atributo es el "tiempo en segundos" que la entrada de directorio correspondiente seguirá existiendo antes de que se desaparezca del directorio. Si el cliente no proporciona un valor para este atributo explícitamente durante la creación del objeto, el DS proporciona un valor predeterminado, tal y como se especifica más adelante.

Una nueva operación LDAP extendida con OID = 1.3.6.1.4.1.1466.101.119.1 para la actualización de cliente de una entrada dinámica en el directorio se definirá y publicará en el atributo **supportedExtension** del objeto DSE raíz.

En la implementación real, **entryTTL** es un atributo construido. La hora de expiración real del objeto se almacena como una hora absoluta en la que el objeto se puede destruir en un atributo solo del sistema denominado **MS-DS-entry-Time-to-Live**.

Todos los objetos dinámicos tienen las siguientes limitaciones:

-   Un objeto dinámico eliminado debido a su expiración de TTL no deja un objeto de desecho detrás.
-   Todos los controladores de sesión que contienen réplicas de objetos dinámicos deben ejecutarse en Windows Server 2003.
-   Las entradas dinámicas con valores de TTL se admiten en todas las particiones excepto la partición de configuración y la partición de esquema.
-   Active Directory Domain Services no publique el atributo **dynamicSubtrees** opcional, como se describe en RFC 2589, en el objeto DSE de raíz.
-   Las entradas dinámicas se administran de forma similar a las entradas no dinámicas al procesar las operaciones de búsqueda, comparación, adición, eliminación, modificación y modifyDN.
-   No hay ninguna manera de cambiar una entrada estática a una entrada dinámica y viceversa.
-   No se puede Agregar una entrada no dinámica subordinada a una entrada dinámica.

 

 




