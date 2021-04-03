---
description: En el procedimiento siguiente se describe un escenario para generar una transformación que oculta una característica de forma permanente.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082931"
---
# <a name="generating-a-transform"></a>Generar una transformación

En el procedimiento siguiente se describe un escenario para generar una transformación que oculta una característica de forma permanente.

**Para ocultar permanentemente una característica del producto**

1.  Copie el paquete de instalación original.
2.  Modifique la copia estableciendo el valor de la columna de visualización de la [tabla de características](feature-table.md) en cero. Esto especifica ocultar la característica.
3.  Cree una transformación desde el paquete de instalación original a los nuevos paquetes de instalación mediante una llamada a [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Cree la información de resumen en la transformación mediante una llamada a [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La transformación está lista para aplicarse durante la instalación. Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).

 

 



