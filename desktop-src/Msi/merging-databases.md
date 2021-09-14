---
description: Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante la realización de una combinación.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Combinar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261284"
---
# <a name="merging-databases"></a>Combinar bases de datos

Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante la realización de una combinación. [Las mezclas y transformaciones funcionan](merges-and-transforms.md) en una base de datos completa y una combinación combina dos bases de datos en una. Las mezclas son útiles para los equipos de desarrollo porque permiten dividir la base de datos de instalación de una aplicación grande en partes más pequeñas y, a continuación, volver a combinarla en la base de datos de instalación completa más adelante.

**Para combinar varias bases de datos de componentes en una base de datos completa única**

1.  Desarrolle las bases de datos de componentes parciales por separado.
2.  Combine cada base de datos de componentes en la base de datos del producto principal mediante una llamada a [**la función MsiDatabaseMerge.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

 



