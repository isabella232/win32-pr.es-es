---
title: In-Process compatibilidad
description: La implementación actual de anotación dinámica está completamente en proceso y, por tanto, solo permite que el proceso propietario de esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567432"
---
# <a name="in-process-support"></a>In-Process compatibilidad

La implementación actual de anotación dinámica está completamente en proceso y, por tanto, solo permite que el proceso propietario de esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario. No es posible que un proceso anote los elementos de la interfaz de usuario de otro proceso.

Tenga en cuenta que esto solo afecta al acto de establecer una anotación; no interfiere con la capacidad de los clientes de acceder a las propiedades (anotadas o de otro modo) de los elementos de la interfaz de usuario en otros procesos.

 

 




