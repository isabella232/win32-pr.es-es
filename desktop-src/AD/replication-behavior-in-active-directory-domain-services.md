---
title: Comportamiento de replicación en Active Directory Domain Services
description: El comportamiento de replicación es coherente y predecible. Dado un conjunto de cambios en una réplica determinada, el resultado se puede predecir \ 8212; los cambios se propagarán a todas las demás réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory , Replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7548ecf146f1d23b97b9db6a0307b21a6c39d359576c2de02285331d165fad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025143"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportamiento de replicación en Active Directory Domain Services

El comportamiento de replicación es coherente y predecible. Dado un conjunto de cambios en una réplica determinada, se puede predecir el resultado: los cambios se propagarán a todas las demás réplicas. Es imposible diseñar un modelo general confiable para predecir cuándo se aplicarán los cambios en todas las demás réplicas, o en una réplica determinada, porque no se puede conocer el estado futuro del sistema distribuido en su conjunto. Esto se denomina "latencia no determinista", y las aplicaciones que usan el directorio deben comprenderlo y permitirlo.

La situación no es tan compleja en su caso. Solo hay tres estados que una aplicación debe dar cabida:

-   Sesgo de versión: ninguno de los cambios que se aplican a una réplica de origen determinada se ha propagado a una réplica de destino determinada. Una aplicación que lee la réplica de origen ve la nueva versión de la información, mientras que una aplicación que lee el destino ve la versión anterior (o nada, si la nueva información se agregó por primera vez). La asimetría de versiones se aplica a todos los consumidores del servicio de directorio.
-   Actualización parcial: algunos de los cambios que se aplican a una réplica de origen determinada se han propagado a una réplica de destino determinada. Una aplicación que lee la réplica de origen ve la nueva información, mientras que una aplicación que lee el destino ve una combinación de información antigua y nueva (o solo parte de la nueva información, si la nueva información se agregó por primera vez). La actualización parcial se aplica a los consumidores del servicio de directorio que usan dos o más objetos relacionados para almacenar su información.
-   Estado totalmente replicado: todos los cambios que se aplican a una réplica de origen determinada se han propagado a una réplica de destino determinada. Las aplicaciones de las réplicas de origen y destino ven la misma información.

 

 




