---
title: Por qué Active Directory Domain Services usa este modelo de replicación
description: En este tema se explican los motivos del sistema de forma libre usado por Active Directory Domain Services para un modelo de replicación.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Active Directory del modelo de replicación, ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903088"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Por qué Active Directory Domain Services usa este modelo de replicación

En este tema se explican los motivos del sistema de forma libre usado por Active Directory Domain Services para un modelo de replicación.

Active Directory Domain Services son un sistema de forma libre por los siguientes motivos:

-   Los clientes requieren una solución muy distribuida en la que se puedan distribuir partes del directorio en sus redes y administrarse localmente.
-   A menudo, los clientes de gran tamaño crecen hasta millones de objetos, cientos o miles de réplicas, o ambos.
-   Muchas redes de clientes solo proporcionan conectividad intermitente a algunas ubicaciones; por ejemplo, las plataformas de perforación de petróleo remoto y se distribuyen al mar, por lo que el sistema debe ser tolerante a las operaciones parcialmente conectadas o desconectadas.

No hay ninguna manera de garantizar el conocimiento completo del estado actual o futuro de un sistema distribuido, ya que el conocimiento de los cambios de estado se debe propagar y la propagación lleva tiempo, durante el cual pueden producirse más cambios de estado.

Los sistemas estrechamente acoplados controlan la incertidumbre al intentar eliminarlo. Esto se logra a través de las restricciones en las actualizaciones, que requieren que todos los nodos o la mayoría de los nodos estén disponibles antes de que se puedan realizar actualizaciones, mediante esquemas de bloqueo distribuidos o un solo maestro para los recursos críticos, restringiendo todos los nodos para que estén bien conectados o alguna combinación de estas técnicas. Cuanto más estrechamente se acoplan los nodos informáticos en un sistema distribuido, menor es el límite de escalado.

Los sistemas de forma libre controlan la incertidumbre al tolerarlas. Un sistema de forma libre permite que los nodos tengan vistas diferentes del estado general del sistema y proporciona algoritmos para resolver conflictos.

Las soluciones estrechamente acopladas se rechazaron como inadecuadas para Active Directory Domain Services debido a los requisitos de administración local, operación desconectada y escalabilidad a un gran número de nodos. El modelo de acoplamiento flexible elegido, coherencia flexible de varios maestros con convergencia, satisface todos los requisitos.

 

 




