---
title: Replicación e integridad de los datos
description: Active Directory Domain Services proporcionar una actualización de varios maestros.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, la replicación y la integridad de los datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656219"
---
# <a name="replication-and-data-integrity"></a>Replicación e integridad de los datos

Active Directory Domain Services proporcionar *una actualización de varios maestros*. La actualización de varios maestros significa que se pueden escribir todas las réplicas completas de una partición determinada (las réplicas parciales en los servidores de catálogo global no se pueden escribir). La actualización de varios maestros significa que las actualizaciones no se bloquean aunque algunas réplicas no funcionen. El servidor de Active Directory propaga los cambios de la réplica actualizada a todas las demás réplicas. La replicación es automática y transparente.

Para obtener más información, vea los siguientes temas.

-   [El modelo de replicación en Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Comportamiento de la replicación en Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Detección y prevención de la latencia de replicación](detecting-and-avoiding-replication-latency.md)

 

 




