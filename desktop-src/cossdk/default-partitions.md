---
description: Particiones predeterminadas
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Particiones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466973"
---
# <a name="default-partitions"></a>Particiones predeterminadas

Cuando se asigna una partición predeterminada a un usuario, COM+ intenta activar primero los componentes de esa partición. Si se produce un error en la activación, COM+ busca en la partición global el componente que se debe activar. La excepción a este proceso se produce cuando el componente COM+ incluye un moniker de partición, que especifica explícitamente la partición en la que se encuentra el componente. En este caso, el moniker de partición tiene prioridad sobre cualquier configuración de partición predeterminada.

Cuando se usan particiones locales, la partición predeterminada se asigna a los usuarios mediante la carpeta Usuarios de particiones **COM+** de la herramienta administrativa Servicios de componentes del servidor de aplicaciones. Cuando se usan conjuntos de particiones Active Directory, la partición predeterminada del usuario viene determinada por el conjunto de particiones del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones locales](local-partitions.md)
</dt> <dt>

[Propiedades de partición](partition-properties.md)
</dt> <dt>

[Particiones y Active Directory](partitions-and-active-directory.md)
</dt> <dt>

[La partición global](the-global-partition.md)
</dt> </dl>

 

 



