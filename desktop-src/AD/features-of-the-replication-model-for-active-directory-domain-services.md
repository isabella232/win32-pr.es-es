---
title: Características del modelo de replicación para Active Directory Domain Services
description: El modelo de replicación usado en Active Directory Domain Services se denomina coherencia flexible de varios maestros con convergencia.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modelo de replicación
- Características del modelo de replicación Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189536"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Características del modelo de replicación para Active Directory Domain Services

El modelo de replicación usado en Active Directory Domain Services se denomina *coherencia flexible de varios* maestros con convergencia . En este modelo, el directorio puede tener muchas réplicas; Un sistema de replicación propaga los cambios realizados en cualquier réplica determinada a todas las demás réplicas. No se garantiza que las réplicas sean coherentes entre sí en un momento determinado ("coherencia flexible"), ya que los cambios se pueden aplicar a cualquier réplica en cualquier momento ("varios maestros"). Si el sistema puede alcanzar un estado estable, en el que no se producen actualizaciones nuevas y todas las actualizaciones anteriores se han replicado completamente, se garantiza que todas las réplicas convergen en el mismo conjunto de valores ("convergencia").

 

 




