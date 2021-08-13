---
description: Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante la realización de una combinación.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Combinación de bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628711"
---
# <a name="merging-databases"></a>Combinación de bases de datos

Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante la realización de una combinación. [Las mezclas y transformaciones funcionan](merges-and-transforms.md) en una base de datos completa y una combinación combina dos bases de datos en una. Las mezclas son útiles para los equipos de desarrollo porque permiten dividir la base de datos de instalación de una aplicación grande en partes más pequeñas y, a continuación, volver a combinarla en la base de datos de instalación completa más adelante.

**Para combinar varias bases de datos de componentes en una sola base de datos completa**

1.  Desarrolle las bases de datos de componentes parciales por separado.
2.  Combine cada base de datos de componentes en la base de datos del producto principal mediante una llamada a la [**función MsiDatabaseMerge.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

 



