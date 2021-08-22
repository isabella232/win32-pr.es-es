---
description: Si un experto no funciona durante el tiempo de ejecución, si usa Monitor de red para la administración de memoria, Monitor de red liberará la memoria asignada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4cc5b38f5525b7c0d19e115c83ed9f770c72215c6b64825a089ec389bfc09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555885"
---
# <a name="managing-memory"></a>Administración de memoria

Si un experto no funciona durante el tiempo de ejecución, si usa Monitor de red para la administración de memoria, Monitor de red liberará la memoria asignada. Sin embargo, al escribir un experto, podría ser necesario adquirir información sobre los recursos del sistema y la estructura de datos. Por ejemplo, el Monitor de red de uso de protocolos de compilación adquiere un identificador de archivo para crear una nueva captura. Cada experto debe crear su propio control **try/catch** para que el experto pueda liberar los recursos que adquirió.

Cuando se asigna memoria, use las siguientes funciones de memoria existentes:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



