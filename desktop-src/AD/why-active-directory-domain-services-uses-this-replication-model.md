---
title: Por qué Active Directory Domain Services este modelo de replicación
description: En este tema se explican las razones del sistema de forma libre que usa Active Directory Domain Services para un modelo de replicación.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Replication Model Active Directory ,advantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c137fadf768c97b6d8be962b22c74b45e30bc41c7dfb7e9ea67e1f145cd92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181996"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Por qué Active Directory Domain Services este modelo de replicación

En este tema se explican las razones del sistema de forma libre que usa Active Directory Domain Services para un modelo de replicación.

Active Directory Domain Services son un sistema de forma libre por los siguientes motivos:

-   Los clientes requieren una solución altamente distribuida en la que las partes del directorio se pueden distribuir entre sus redes y administrarse localmente.
-   Los clientes grandes suelen crecer hasta millones de objetos, cientos o miles de réplicas, o ambos.
-   Muchas redes de clientes solo proporcionan conectividad intermitente a algunas ubicaciones. por ejemplo, las plataformas de exploración de petróleo remotas y los envíos en el mar, por lo que el sistema debe ser tolerante a las operaciones parcialmente conectadas o desconectadas.

No hay ninguna manera de garantizar un conocimiento completo del estado actual o futuro de un sistema distribuido, ya que el conocimiento de los cambios de estado debe propagarse y la propagación lleva tiempo, durante el cual pueden producirse más cambios de estado.

Los sistemas estrechamente acoplados controlan la incertidumbre al intentar eliminarla. Esto se logra mediante restricciones en las actualizaciones, que requieren que todos los nodos o la mayoría de los nodos estén disponibles antes de que se puedan realizar las actualizaciones, mediante esquemas de bloqueo distribuido o una arquitectura única para recursos críticos, la restricción de que todos los nodos estén bien conectados o alguna combinación de estas técnicas. Entre más estrechamente acoplados estén los nodos informáticos de un sistema distribuido, menor es el límite de escalado.

Los sistemas de forma libre controlan la incertidumbre tolerando esta situación. Un sistema de forma libre permite que los nodos tengan vistas diferentes del estado general del sistema y proporciona algoritmos para resolver conflictos.

Las soluciones estrechamente acopladas se rechazaron como no adecuadas para Active Directory Domain Services debido a los requisitos de administración local, funcionamiento desconectado y escalabilidad a un número muy grande de nodos. El modelo de acoplamiento flexible elegido, coherencia flexible de varios maestros con convergencia, satisface todos los requisitos.

 

 




