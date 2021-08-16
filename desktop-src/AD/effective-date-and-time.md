---
title: Fecha y hora efectivas
description: La fecha y hora efectivas es una estrategia de prevención que evita la asimetría de versiones y las actualizaciones parciales al aplazar los datos efectivos de la información a algún momento en el futuro cuando el cambio tiene una alta probabilidad de que se replique por completo.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d95c80627c878bbc9d8cb6ac16436e6dae3e12cf262e797724cd5053f371ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695368"
---
# <a name="effective-date-and-time"></a>Fecha y hora efectivas

 La fecha y hora efectivas es una estrategia de prevención que evita la asimetría de versiones y las actualizaciones parciales al aplazar los datos efectivos de la información a algún momento en el futuro cuando el cambio tiene una alta probabilidad de que se replique por completo. Para implementar fechas efectivas, los objetos de aplicación deben incluir una marca de tiempo de fecha efectiva, que se rellena cuando se crea o cambia el objeto. Los consumidores de los objetos comprueban la marca de tiempo y aplazan el uso de los objetos hasta que se alcanza esa fecha y hora.

Algunas consideraciones importantes:

-   Las aplicaciones que eligen este enfoque deben asegurarse de que hay un conjunto de datos aplicables que se usarán hasta que los objetos actualizados entren en vigor.
-   El servicio de hora distribuido Windows NT 4.0 mantiene sincronizados los relojes de la Windows 2000. Sin embargo, ningún servicio de hora es perfecto, por lo que hay una pequeña ventana para la asimetría de versiones.
-   Si se establece una fecha efectiva, se supone que conoce la latencia de replicación general del sistema distribuido en cuestión. En una red estable, una buena regla general para las fechas efectivas es la (hora de la actualización) + (2 \* (latencia total media)). Por lo tanto, para un sistema cuya latencia general promedia 4 horas, un retraso de 8 horas es razonable.
-   En una red inestable, determinar un valor "bueno" para las fechas efectivas es mucho más difícil, ya que la latencia puede ser muy variable. La fecha efectiva es más "eficaz" en una red inestable cuando se combina con otras estrategias de prevención o detección, como sumas de comprobación o GUID de coherencia. Para obtener más información, vea [Sumas de comprobación y Recuentos de objetos](checksums-and-object-counts.md).

 

 




