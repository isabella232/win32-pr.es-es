---
title: Objetos dinámicos
description: En Windows Server 2003 y versiones posteriores de Windows, Active Directory Domain Services para almacenar entradas dinámicas en el directorio.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- objetos dinámicos de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191723"
---
# <a name="dynamic-objects"></a>Objetos dinámicos

En Windows Server 2003 y versiones posteriores de Windows, Active Directory Domain Services para almacenar entradas dinámicas en el directorio. Una entrada dinámica es un objeto del directorio que tiene un valor de período de vida (TTL) asociado. El TTL de una entrada se establece cuando se crea la entrada. El período de vida se disminuye automáticamente y, cuando expira, desaparece la entrada dinámica. El cliente puede hacer que una entrada dinámica permanezca más tiempo que su vida restante actual actualizando (modificando) su valor TTL. Los clientes que almacenan datos dinámicos en el directorio deben actualizar periódicamente los datos para evitar que desaparezcan.

Muchas aplicaciones y servicios que usan LDAP para almacenar y acceder a datos relativamente estáticos e interesantes globalmente desde un servidor Active Directory también preferirán seguir usando el acceso LDAP para sus necesidades de datos dinámicos. Además, para algunas aplicaciones, puede ser conveniente desactivar la carga de la tarea de recolección de elementos no utilizados en el DS que tienen una vida útil limitada para el servicio de directorio. Las particiones de directorio de aplicación (con la capacidad para la colocación controlada de réplicas) y los TCL por objeto juntos proporcionarán la capacidad de hospedar datos dinámicos en Active Directory Domain Services, lo que permite el acceso LDAP a ellos.

Una nueva clase de objeto auxiliar denominada **dynamicObject** con OID = 1.3.6.1.4.1.1466.101.119.2 se definirá en el esquema base de AD que usarán las entradas dinámicas. Esta clase auxiliar contiene el atributo **denominado entryTTL** con OID = 1.3.6.1.4.1.1466.101.119.3 como atributo system-may-contain. El valor de este atributo es el "tiempo en segundos" que seguirá existiendo la entrada de directorio correspondiente antes de desaparecer del directorio. Si el cliente no proporciona un valor para este atributo explícitamente durante la creación del objeto, el DS proporciona un valor predeterminado como se especifica más adelante.

Una nueva operación LDAP extendida con OID = 1.3.6.1.4.1.1466.101.119.1 para la actualización de cliente de una entrada dinámica en el directorio se definirá y publicará en el atributo **supportedExtension** del objeto DSE raíz.

En la implementación real, **entryTTL** es un atributo construido. La hora de expiración del objeto real se almacena como una hora absoluta en la que el objeto se puede destruir en un atributo solo del sistema denominado **ms-DS-Entry-Time-To-Live**.

Todos los objetos dinámicos tienen las siguientes limitaciones:

-   Un objeto dinámico eliminado debido a su expiración del TTL no deja un lápido.
-   Todos los DCs que tienen réplicas de objetos dinámicos deben ejecutarse Windows Server 2003.
-   Las entradas dinámicas con valores TTL se admiten en todas las particiones, excepto en la partición de configuración y en la partición esquema.
-   Active Directory Domain Services publicar el atributo **dynamicSubtrees** opcional, como se describe en RFC 2589, en el objeto DSE raíz.
-   Las entradas dinámicas se controlan de forma similar a las entradas no dinámicas al procesar operaciones de búsqueda, comparación, adición, eliminación, modificación y modificaciónDN.
-   No hay ninguna manera de cambiar una entrada estática en una entrada dinámica y viceversa.
-   No se puede agregar una entrada no dinámica subordinada a una entrada dinámica.

 

 




