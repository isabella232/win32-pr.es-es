---
description: La partición global
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: La partición global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fd66e8bb4401465a604b187d8638b60993b45c130d18ab2c4c5d054d9686d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636795"
---
# <a name="the-global-partition"></a>La partición global

Además de las particiones definidas por el administrador y los conjuntos de particiones, hay una partición especial en cada equipo denominada partición *global*. Cuando se instala COM+, se crea automáticamente una partición global. La partición global está diseñada para contener aplicaciones de todo el sistema que deben ser accesibles para todos los usuarios de un servidor o del dominio. La instalación de una aplicación en la partición global elimina la necesidad de instalar una copia de la aplicación en el conjunto de particiones de cada usuario individual.

Si el conjunto de particiones de un usuario no incluye una aplicación específica a la que el usuario está intentando acceder, pero esa aplicación está instalada en la partición global, la aplicación se activa desde la partición global. En este caso, sin embargo, todos los componentes de la aplicación instalados en la partición global deben marcarse como componentes públicos, no privados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones predeterminadas](default-partitions.md)
</dt> <dt>

[Particiones locales](local-partitions.md)
</dt> <dt>

[Propiedades de partición](partition-properties.md)
</dt> <dt>

[Particiones y Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



