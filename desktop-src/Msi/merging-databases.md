---
description: Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante una combinación.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Combinar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002559"
---
# <a name="merging-databases"></a>Combinar bases de datos

Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante una combinación. Las [combinaciones y transformaciones](merges-and-transforms.md) operan en una base de datos completa y una combinación combina dos bases de datos en una. Las combinaciones son útiles para los equipos de desarrollo porque permiten que la base de datos de instalación de aplicaciones de gran tamaño se divida en partes más pequeñas y, posteriormente, se vuelvan a combinar en la base de datos de instalación completa.

**Para combinar varias bases de datos de componentes en una sola base de datos completa**

1.  Desarrolle las bases de datos de componentes parciales por separado.
2.  Combine cada base de datos de componentes en la base de datos principal del producto llamando a la función [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .

 

 



