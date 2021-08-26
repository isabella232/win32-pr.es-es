---
title: Realización de una llamada a procedimiento remoto
description: Una vez que el programa cliente de aplicaciones distribuidas que usa identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Llamada a procedimiento remoto RPC , tareas, realizar una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020085"
---
# <a name="making-a-remote-procedure-call"></a>Realización de una llamada a procedimiento remoto

Una vez que el programa cliente de aplicaciones distribuidas que usa identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.

Rpc de Microsoft también ofrece identificadores de enlace personalizados, identificadores de enlace implícitos y identificadores de enlace automático. Estos identificadores de enlace ofrecen programas cliente y servidor diferentes niveles de control sobre el proceso de ejecución de procedimientos remotos. Para obtener más información sobre los distintos tipos de identificadores y la flexibilidad que ofrecen, vea [Enlace y identificadores.](binding-and-handles.md)

Para ejecutar la llamada a procedimiento de forma remota, llame a la función de código auxiliar del lado cliente de la misma manera que se llama a cualquier función de C.

 

 




