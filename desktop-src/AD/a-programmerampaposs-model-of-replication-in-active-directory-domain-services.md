---
title: Modelo de replicación de un programador en Active Directory Domain Services
description: A continuación se muestra una descripción del modelo de replicación para Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Un modelo de programador de Active Directory Replication AD
- Modelo de replicación de un programador en Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b758a31913d0c306105d0d3ce51e72607530e314d79601e8e5230495458d9793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841235"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Modelo de replicación de un programador en Active Directory Domain Services

A continuación se muestra una descripción del modelo de replicación para Active Directory Domain Services.

Todas las actualizaciones del controlador de Dominio de Active Directory (DC) se realizan mediante solicitudes LDAP que crean, modifican o eliminan un objeto para cada solicitud. Una única solicitud puede establecer o modificar varios atributos en un objeto .

Una solicitud de actualización se procesa como una transacción atómica en algún controlador de dominio. Se produce la actualización completa o no se produce ninguna. Si el solicitante recibe una respuesta correcta a una solicitud de actualización, esa solicitud completa se ha realizado correctamente (se ha confirmado). Esto se denomina "escritura de origen". No se pueden agrupar varias solicitudes LDAP en una única transacción mayor.

En una escritura de origen, un controlador de dominio calcula un "stamp" para cada valor de atributo nuevo o modificado y asocia este stamp al valor para que, cuando se replique el valor, el stamp también se replique. El nuevo stamp es único y, en el caso de una actualización, el nuevo stamp es mayor que el stamp del valor anterior en ese controlador de dominio.

En ocasiones, un controlador de dominio selecciona el conjunto de objetos que han cambiado desde la última vez que el controlador de dominio realizó la replicación. A continuación, para cada objeto, envía un único mensaje a todos los demás DCs que contienen todos los valores actuales de atributos cambiados desde la última vez que se replicó el objeto. Los mensajes de replicación son confiables y se entregan en orden, pero pueden requerir más tiempo para entregarse.

Cuando un controlador de dominio recibe un mensaje de replicación de otro controlador de dominio, lo procesa de la siguiente manera: para cada atributo modificado, si la marca del valor del mensaje de replicación es mayor que la marca en el valor actual, el controlador de dominio aplica la actualización. De lo contrario, el controlador de dominio descarta la actualización. Cada mensaje de replicación se aplica como una transacción atómica, al igual que una escritura de origen.

Este es el modelo Active Directory Domain Services replicación. Las propiedades clave de este modelo incluyen:

-   Una escritura que se origina en un único objeto es atómica.
-   Al replicar cambios, se envían todos los cambios realizados por una escritura de origen o ninguno de ellos.
-   Una escritura replicada en un único objeto es atómica, pero los conflictos se resuelven atributo a atributo.

El modelo no garantiza el orden de replicación de los cambios realizados en objetos diferentes. No escriba aplicaciones que supongan que los cambios se replican en orden de escritura de origen. El modelo no garantiza que si un atributo de un objeto se cambia dos veces, se replicarán ambos valores. La replicación envía solo el valor actual en el momento de la replicación.

El modelo difiere de la realidad de varias maneras que solo afectan al rendimiento. Por ejemplo, Active Directory Server envía mensajes de replicación que contienen los cambios en varios objetos, pero procesa el contenido de un mensaje de varios objetos como si fuera una serie de mensajes de un solo objeto. El Active Directory Server no realiza la replicación punto a punto como se describe en el modelo, sino que realiza una replicación transitiva más compleja y eficaz que es funcionalmente equivalente al modelo.

 

 




