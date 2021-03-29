---
description: Si se produce un error en el experto durante el tiempo de ejecución, si utiliza Monitor de red funciones para la administración de memoria, Monitor de red liberará memoria asignada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Administrar memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001235"
---
# <a name="managing-memory"></a>Administrar memoria

Si se produce un error en el experto durante el tiempo de ejecución, si utiliza Monitor de red funciones para la administración de memoria, Monitor de red liberará memoria asignada. Sin embargo, cuando se escribe un experto, podría ser necesario adquirir recursos del sistema e información de la estructura de datos. Por ejemplo, el experto de combinación de protocolos de Monitor de red adquiere un identificador de archivo para crear una nueva captura. Cada experto debe crear su propio control **try/catch** para que el experto pueda liberar los recursos adquiridos.

Cuando se asigna la memoria, use las siguientes funciones de memoria existentes:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



