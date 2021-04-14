---
description: La partición global
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: La partición global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496649"
---
# <a name="the-global-partition"></a>La partición global

Además de las particiones y los conjuntos de particiones definidos por el administrador, hay una partición especial en cada equipo denominada *partición global*. Cuando se instala COM+, se crea automáticamente una partición global. La partición global está diseñada para contener aplicaciones para todo el sistema que deben ser accesibles para todos los usuarios de un servidor o en el dominio. La instalación de una aplicación en la partición global elimina la necesidad de instalar una copia de la aplicación en cada conjunto de particiones de usuario individual.

Si el conjunto de particiones de un usuario no incluye una aplicación específica a la que el usuario está intentando tener acceso, pero esa aplicación se instala en la partición global, la aplicación se activa desde la partición global. Sin embargo, en este caso, todos los componentes de la aplicación instalados en la partición global deben estar marcados como componentes públicos, no privados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones predeterminadas](default-partitions.md)
</dt> <dt>

[Particiones locales](local-partitions.md)
</dt> <dt>

[Propiedades de la partición](partition-properties.md)
</dt> <dt>

[Particiones y Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



