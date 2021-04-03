---
title: Fecha y hora efectivas
description: La fecha y hora efectivas es una estrategia de prevención que evita el sesgo de la versión y las actualizaciones parciales al aplazar los datos efectivos de la información a algún punto del futuro cuando el cambio tiene una alta probabilidad de que se replique por completo.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075138"
---
# <a name="effective-date-and-time"></a>Fecha y hora efectivas

La *fecha y hora efectivas* es una estrategia de prevención que evita el sesgo de la versión y las actualizaciones parciales al aplazar los datos efectivos de la información a algún punto del futuro cuando el cambio tiene una alta probabilidad de que se replique por completo. Para implementar fechas efectivas, los objetos de aplicación deben incluir una marca de tiempo de fecha efectiva, que se rellena cuando se crea o cambia el objeto. Los consumidores de los objetos comprueban la marca de tiempo y aplazan el uso de los objetos hasta que se alcanza esa fecha y hora.

Algunas consideraciones importantes:

-   Las aplicaciones que eligen este enfoque deben asegurarse de que haya un conjunto de datos aplicables para usar hasta que los objetos actualizados surtan efecto.
-   El servicio de hora distribuida en Windows NT 4,0 mantiene sincronizados los relojes de la sincronización de Windows 2000. Sin embargo, no hay ningún servicio de hora perfecto, por lo que hay una pequeña ventana para el sesgo de la versión.
-   La configuración de una buena fecha efectiva presupone el conocimiento de la latencia general de replicación para el sistema distribuido en cuestión. En una red estable, una buena regla general para las fechas efectivas es la (hora de la actualización) + (2 \* (latencia total media)). Por lo tanto, para un sistema cuya latencia total promedio sea de 4 horas, un retraso de 8 horas es razonable.
-   En una red inestable, es mucho más difícil determinar un valor "bueno" para las fechas efectivas, ya que la latencia puede ser muy variable. La fecha efectiva es la más "efectiva" en una red inestable cuando se combina con otras estrategias de prevención o detección, como sumas de comprobación o GUID de coherencia. Para obtener más información, vea [sumas de comprobación y recuentos de objetos](checksums-and-object-counts.md).

 

 




