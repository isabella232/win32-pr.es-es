---
title: Compatibilidad con In-Process
description: La implementación actual de la anotación dinámica está completamente en proceso y, por consiguiente, solo permite que el proceso que posee esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356840"
---
# <a name="in-process-support"></a>Compatibilidad con In-Process

La implementación actual de la anotación dinámica está completamente en proceso y, por consiguiente, solo permite que el proceso que posee esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario. No es posible que un proceso anote los elementos de la interfaz de usuario de otro proceso.

Tenga en cuenta que esto solo afecta a la acción de establecer una anotación; no interfiere con la posibilidad de que los clientes tengan acceso a las propiedades (anotadas o de otro tipo) de los elementos de la interfaz de usuario en otros procesos.

 

 




