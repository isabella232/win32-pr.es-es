---
description: Una transformación es una colección de cambios aplicados a una instalación de. Al aplicar una transformación a un paquete de instalación base, el instalador puede Agregar o reemplazar datos en la base de datos de instalación. El instalador solo puede aplicar transformaciones durante una instalación.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Acerca de las transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276537"
---
# <a name="about-transforms"></a>Acerca de las transformaciones

Una transformación es una colección de cambios aplicados a una instalación de. Al aplicar una transformación a un paquete de instalación base, el instalador puede Agregar o reemplazar datos en la base de datos de instalación. El instalador solo puede aplicar transformaciones durante una instalación.

El instalador registra una lista de transformaciones requeridas por el producto durante la instalación. El instalador debe aplicar estas transformaciones al paquete de instalación del producto al configurar o instalar el producto. Si una transformación enumerada no está disponible y la resistencia de origen de la transformación no puede restaurarla, se producirá un error en la instalación.

Una transformación puede modificar la información que se encuentra en cualquier tabla persistente en la [base de datos del instalador](installer-database.md). Una transformación también puede Agregar o quitar tablas persistentes en la base de datos del instalador. Las transformaciones no pueden modificar ninguna parte de un paquete de instalación que no esté en una tabla de base de datos, como la información de la [secuencia de información de Resumen](summary-information-stream.md), la información de los subalmacenamientos o los archivos de los archivados incrustados.

Las transformaciones tienen una secuencia de información de resumen que puede contener condiciones de validación y condiciones de error. La validación de transformación y las condiciones de error se pueden agregar a la información de Resumen mediante la función [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . Las condiciones de validación controlan si el instalador puede aplicar la transformación a una base de datos de instalación determinada. La validación de la transformación puede estar condicionada a los valores de las propiedades [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) y [**ProductLanguage**](productlanguage.md) especificadas en la transformación y en las de la base de datos de instalación. Las condiciones de error de transformación controlan qué errores se suprimen cuando se aplica la transformación. Las condiciones de error incluidas en la transformación se reemplazan por las condiciones de error especificadas mediante los métodos [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) y [**ApplyTransform**](database-applytransform.md) .

> [!Note]  
> Las transformaciones de personalización típicas no tienen condiciones de validación ni se validan con el [**ProductCode**](productcode.md). Las transformaciones almacenadas en [paquetes de revisión](patch-packages.md) tienen generalmente condiciones de validación estrictas para garantizar que se aplica la transformación correcta al destino de la revisión.

 

Hay tres tipos de transformaciones de Windows Installer:

-   [Transformaciones incrustadas](embedded-transforms.md)
-   [Transformaciones protegidas](secured-transforms.md)
-   [Transformaciones no seguras](unsecured-transforms.md)

 

 



