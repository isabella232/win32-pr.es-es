---
description: Conceptos de particiones COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Conceptos de particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496061"
---
# <a name="com-partitions-concepts"></a>Conceptos de particiones COM+

En entornos informáticos en los que es necesario utilizar diferentes versiones o configuraciones de una aplicación en el mismo equipo, pueden producirse conflictos cuando una versión de la aplicación requiere componentes diferentes a los otros o cuando una versión requiere un componente en el equipo que no es compatible con la otra versión de la aplicación. En el pasado, la única manera de resolver este problema era mantener varios equipos y ejecutar una versión diferente de la aplicación en cada equipo. Este enfoque es costoso e ineficaz porque aumenta los costos de hardware y la sobrecarga administrativa.

COM+ soluciona este problema proporcionando la característica de particiones de COM+. Puede usar particiones COM+ para instalar diferentes versiones de una aplicación COM+ en un equipo y ejecutarlas simultáneamente.

Para comprender y usar esta característica, vea los temas siguientes:

-   [¿Qué son las particiones COM+?](what-are-com--partitions-.md)
-   [Implementación de particiones](partition-implementation.md)
-   [Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
-   [Particiones y componentes en cola de COM+](com--queued-components-and-partitions.md)
-   [Restricciones de diseño de aplicaciones](application-design-restrictions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de particiones COM+](com--partitions-tasks.md)
</dt> </dl>

 

 



