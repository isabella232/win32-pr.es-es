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
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656234"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Características del modelo de replicación para Active Directory Domain Services

El modelo de replicación usado en Active Directory Domain Services se denomina *coherencia flexible de varios maestros con convergencia*. En este modelo, el directorio puede tener muchas réplicas; un sistema de replicación propaga los cambios realizados en una réplica determinada a todas las demás réplicas. No se garantiza que las réplicas sean coherentes entre sí en un momento determinado ("coherencia relajada"), ya que los cambios se pueden aplicar a cualquier réplica en cualquier momento ("varios maestros"). Si el sistema puede llegar a un estado estable, en el que no se están produciendo nuevas actualizaciones y todas las actualizaciones anteriores se han replicado por completo, se garantiza que todas las réplicas convergen en el mismo conjunto de valores ("convergencia").

 

 




