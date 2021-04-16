---
title: Controladores COM
description: El propósito de los controladores COM es proporcionar algún 0034; Smart \ 0034; código en el espacio de direcciones del cliente que puede optimizar las llamadas entre un cliente y un servidor. Los controladores pueden invalidar algunas interfaces mientras delegan a otras personas directamente en el servidor (a través del proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714123"
---
# <a name="com-handlers"></a>Controladores COM

El propósito de los controladores COM es proporcionar código "inteligente" en el espacio de direcciones del cliente que puede optimizar las llamadas entre un cliente y un servidor. Los controladores pueden invalidar algunas interfaces mientras delegan a otras personas directamente en el servidor (a través del proxy).

Hay dos tipos de controladores COM:

-   [El controlador OLE](the-ole-handler.md) es un archivo dll pesado que proporciona servicios importantes para la vinculación y la incrustación. Normalmente se crea antes de que se inicie el servidor y se inicializa para que el servidor se active cuando el objeto incrustado entra en el estado de ejecución.
-   [El controlador del lado cliente ligero](the-lightweight-client-side-handler.md) se puede crear para cualquier propósito, puede ser muy pequeño y no se puede crear antes que el servidor.

 

 




