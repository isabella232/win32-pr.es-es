---
description: Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como partición global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementación de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3014aac80e853ca387538faf034eeadae91dd70cf36931de34638cbcbec7b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047353"
---
# <a name="partition-implementation"></a>Implementación de partición

Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como partición *global*. La partición global incluye un conjunto estándar de aplicaciones COM+. Las aplicaciones COM+ que se instalan en la partición global están disponibles automáticamente para todos los usuarios del servidor. Si tiene otras aplicaciones COM+ que desea que estén disponibles para todos los usuarios del servidor, puede agregarlas a la partición global.

Además de la partición global, puede crear otras particiones solo para los usuarios de ese servidor o para los usuarios de todo el dominio. La creación de particiones adicionales e instalación de varias configuraciones de una aplicación COM+ en ellas permite a los usuarios ejecutar esas configuraciones de aplicación simultáneamente en el mismo equipo. Además, al instalar aplicaciones COM+ en una partición que no sea la partición global, puede controlar el acceso de los usuarios a esas aplicaciones.

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición COM+ disponible.

Para obtener más información sobre las particiones locales y las particiones definidas Active Directory, vea los temas siguientes:

-   [Particiones locales](local-partitions.md)
-   [Particiones y Active Directory](partitions-and-active-directory.md)
-   [Particiones predeterminadas](default-partitions.md)
-   [La partición global](the-global-partition.md)
-   [Propiedades de partición](partition-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Componentes y particiones en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



