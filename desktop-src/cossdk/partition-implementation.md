---
description: Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como la partición global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementación de particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714867"
---
# <a name="partition-implementation"></a>Implementación de particiones

Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como la *partición global*. La partición global incluye un conjunto estándar de aplicaciones COM+. Las aplicaciones COM+ que están instaladas en la partición global están disponibles automáticamente para todos los usuarios del servidor. Si tiene otras aplicaciones COM+ que le gustaría poner a disposición de todos los usuarios del servidor, puede agregarlas a la partición global.

Además de la partición global, puede crear otras particiones solo para los usuarios de ese servidor o para los usuarios de todo el dominio. La creación de particiones adicionales y la instalación de varias configuraciones de una aplicación COM+ en ellas permite que los usuarios ejecuten esas configuraciones de aplicación simultáneamente en el mismo equipo. Además, al instalar las aplicaciones COM+ en una partición distinta de la partición global, puede controlar el acceso del usuario a esas aplicaciones.

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición de COM+ disponible.

Para obtener más información sobre las particiones locales y las particiones definidas en Active Directory, vea los temas siguientes:

-   [Particiones locales](local-partitions.md)
-   [Particiones y Active Directory](partitions-and-active-directory.md)
-   [Particiones predeterminadas](default-partitions.md)
-   [La partición global](the-global-partition.md)
-   [Propiedades de la partición](partition-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Particiones y componentes en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



