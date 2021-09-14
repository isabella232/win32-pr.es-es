---
description: En el procedimiento siguiente se describe un escenario para generar una transformación que oculta permanentemente una característica.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074737"
---
# <a name="generating-a-transform"></a>Generar una transformación

En el procedimiento siguiente se describe un escenario para generar una transformación que oculta permanentemente una característica.

**Para ocultar permanentemente una característica de producto**

1.  Copie el paquete de instalación original.
2.  Modifique la copia estableciendo el valor de la columna Mostrar de la [tabla Característica](feature-table.md) en cero. Especifica la ocultación de la característica.
3.  Cree una transformación del paquete de instalación original a los nuevos paquetes de instalación mediante una llamada a [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Cree la información de resumen en la transformación mediante una llamada [**a MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La transformación está lista para aplicarse durante la instalación. Para obtener más información, [vea Aplicar transformaciones.](applying-transforms.md)

 

 



