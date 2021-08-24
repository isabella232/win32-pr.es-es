---
title: In-Process compatibilidad
description: La implementación actual de anotación dinámica está completamente en proceso y, por tanto, solo permite que el proceso propietario de esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82deaa2edd9a5df9fd36bed745d1c07a5542e12837cd3fc97c3ac0bdeab098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614745"
---
# <a name="in-process-support"></a>In-Process compatibilidad

La implementación actual de anotación dinámica está completamente en proceso y, por tanto, solo permite que el proceso propietario de esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario. No es posible que un proceso anote los elementos de la interfaz de usuario de otro proceso.

Tenga en cuenta que esto solo afecta al acto de establecer una anotación; no interfiere con la capacidad de los clientes de acceder a las propiedades (anotadas o de otro modo) de los elementos de la interfaz de usuario en otros procesos.

 

 




