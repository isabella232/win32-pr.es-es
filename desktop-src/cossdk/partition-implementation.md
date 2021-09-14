---
description: Cuando se instala en un servidor de aplicaciones, COM+ crea automáticamente una partición, conocida como partición global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementación de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965147"
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

 

 



