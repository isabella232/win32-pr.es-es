---
title: Realización de una llamada a procedimiento remoto
description: Una vez que el programa cliente de las aplicaciones distribuidas que utiliza identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- RPC llamada a procedimiento remoto, tareas, realizar una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772720"
---
# <a name="making-a-remote-procedure-call"></a>Realización de una llamada a procedimiento remoto

Una vez que el programa cliente de las aplicaciones distribuidas que utiliza identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.

Microsoft RPC también ofrece identificadores de enlace personalizados, identificadores de enlace implícitos y controladores de enlace automáticos. Estos identificadores de enlace ofrecen a los programas de cliente y servidor distintos niveles de control sobre el proceso de ejecución de procedimientos remotos. Para obtener más información sobre los diferentes tipos de identificadores y la flexibilidad que ofrecen, vea [enlazar y controlar](binding-and-handles.md).

Para ejecutar la llamada al procedimiento de forma remota, llame a la función de código auxiliar del lado cliente de la misma manera que se llama a cualquier función de C.

 

 




