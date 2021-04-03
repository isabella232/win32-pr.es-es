---
title: Modelo de replicación de un programador en Active Directory Domain Services
description: A continuación se describe el modelo de replicación para Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Modelo de un programador de Active Directory replicación de AD
- Modelo de replicación de un programador en Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075029"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Modelo de replicación de un programador en Active Directory Domain Services

A continuación se describe el modelo de replicación para Active Directory Domain Services.

Todas las actualizaciones del controlador de Dominio de Active Directory (DC) se realizan mediante solicitudes LDAP que crean, modifican o eliminan un objeto para cada solicitud. Una única solicitud puede establecer o modificar varios atributos en un objeto.

Una solicitud de actualización se procesa como una transacción atómica en algún controlador de dominio. Se produce la actualización completa o ninguna de ellas. Si el solicitante recibe una respuesta correcta a una solicitud de actualización, la solicitud completa se ha realizado correctamente (confirmada). Esto se denomina "escritura de origen". No se pueden agrupar varias solicitudes LDAP en una única transacción mayor.

En una escritura de origen, un controlador de dominio calcula una "marca" para cada valor de atributo nuevo o modificado y asocia esta marca al valor de modo que, cuando se replica el valor, la marca también se replica. La nueva marca es única y, en el caso de una actualización, el nuevo sello es mayor que el de la marca del valor anterior en ese controlador de dominio.

En ocasiones, un controlador de dominio selecciona el conjunto de objetos que han cambiado desde la última vez que el controlador de dominio llevó a cabo la replicación. A continuación, para cada objeto, envía un mensaje único a todos los demás controladores de DC que contienen todos los valores actuales de los atributos modificados desde la última vez que se replicó el objeto. Los mensajes de replicación son confiables y se entregan en orden, pero pueden requerir más tiempo para entregarse.

Cuando un controlador de dominio recibe un mensaje de replicación de otro controlador de dominio, lo procesa de la siguiente manera: para cada atributo modificado, si la marca en el valor del mensaje de replicación es mayor que la marca del valor actual, el controlador de dominio aplica la actualización; de lo contrario, el controlador de dominio descartará la actualización. Cada mensaje de replicación se aplica como una transacción atómica, como una escritura de origen.

Es el Active Directory Domain Services modelo de replicación. Las propiedades clave de este modelo incluyen:

-   Una escritura de origen en un único objeto es atómica.
-   Al replicar los cambios, se envían todos los cambios realizados por una escritura de origen o ninguno de ellos.
-   Una escritura replicada en un único objeto es atómica, pero los conflictos se resuelven por atributo.

El modelo no garantiza la ordenación de la replicación de los cambios realizados en objetos diferentes. No escriba aplicaciones que asuman que los cambios se replican en orden de escritura de origen. El modelo no garantiza que, si un atributo de un objeto se cambia dos veces, se replicarán ambos valores. La replicación solo envía el valor actual en el momento de la replicación.

El modelo difiere de la realidad en varias maneras que solo afectan al rendimiento. Por ejemplo, el servidor de Active Directory envía mensajes de replicación que contienen los cambios a varios objetos, pero procesa el contenido de un mensaje de varios objetos como si fuera una serie de mensajes de un solo objeto. El servidor de Active Directory no realiza la replicación punto a punto como se describe en el modelo, sino que realiza una replicación transitiva más compleja y más eficaz que es funcionalmente equivalente al modelo.

 

 




