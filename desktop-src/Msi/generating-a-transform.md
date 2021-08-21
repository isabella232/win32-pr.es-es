---
description: En el procedimiento siguiente se describe un escenario para generar una transformación que oculta permanentemente una característica.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635993"
---
# <a name="generating-a-transform"></a>Generar una transformación

En el procedimiento siguiente se describe un escenario para generar una transformación que oculta permanentemente una característica.

**Para ocultar permanentemente una característica de producto**

1.  Copie el paquete de instalación original.
2.  Modifique la copia estableciendo el valor de la columna Mostrar de la [tabla Característica](feature-table.md) en cero. Esto especifica la ocultación de la característica.
3.  Cree una transformación del paquete de instalación original a los nuevos paquetes de instalación mediante una llamada a [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Cree la información de resumen en la transformación mediante una llamada [**a MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La transformación está lista para aplicarse durante la instalación. Para obtener más información, [vea Aplicar transformaciones.](applying-transforms.md)

 

 



