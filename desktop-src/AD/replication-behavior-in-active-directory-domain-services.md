---
title: Comportamiento de la replicación en Active Directory Domain Services
description: El comportamiento de la replicación es coherente y predecible. dado un conjunto de cambios en una réplica determinada, el resultado se puede predecir \ 8212; los cambios se propagarán a todas las demás réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory de Active Directory Domain Services, replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903095"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportamiento de la replicación en Active Directory Domain Services

El comportamiento de la replicación es coherente y predecible. dado un conjunto de cambios en una réplica determinada, se puede predecir el resultado; los cambios se propagarán a todas las demás réplicas. La idea de un modelo general confiable para predecir cuándo se aplicarán los cambios en el resto de réplicas, o en una réplica determinada, no es posible, ya que no se puede conocer el estado futuro del sistema distribuido como un todo. Esto se denomina "latencia no determinista" y las aplicaciones que usan el directorio deben comprender y permitirlo.

La situación no es tan compleja en el caso de que aparezca. Hay solo tres Estados que una aplicación debe acomodar:

-   Sesgo de versión: ninguno de los cambios que se aplican a una réplica de origen determinada se ha propagado a una réplica de destino determinada. Una aplicación que lee la réplica de origen ve la nueva versión de la información, mientras que una aplicación que lee el destino ve la versión anterior (o nada, si la nueva información se agregó por primera vez). El sesgo de versión se aplica a todos los consumidores del servicio de directorio.
-   Actualización parcial: algunos de los cambios que se aplican a una réplica de origen determinada se han propagado a una réplica de destino determinada. Una aplicación que lee la réplica de origen ve la nueva información, mientras que una aplicación que lee el destino ve una mezcla de información antigua y nueva (o solo parte de la nueva información, si la nueva información se agregó por primera vez). La actualización parcial se aplica a los consumidores del servicio de directorio que usan dos o más objetos relacionados para almacenar su información.
-   Estado totalmente replicado: todos los cambios que se aplican a una réplica de origen determinada se propagan a una réplica de destino determinada. Las aplicaciones en las réplicas de origen y de destino ven la misma información.

 

 




