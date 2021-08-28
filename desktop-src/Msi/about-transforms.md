---
description: Una transformación es una colección de cambios aplicados a una instalación. Al aplicar una transformación a un paquete de instalación base, el instalador puede agregar o reemplazar datos en la base de datos de instalación. El instalador solo puede aplicar transformaciones durante una instalación.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Acerca de las transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635430fb5e75b658880d5c5670219cae950502421c2b188af0381fd60ad3d48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013273"
---
# <a name="about-transforms"></a>Acerca de las transformaciones

Una transformación es una colección de cambios aplicados a una instalación. Al aplicar una transformación a un paquete de instalación base, el instalador puede agregar o reemplazar datos en la base de datos de instalación. El instalador solo puede aplicar transformaciones durante una instalación.

El instalador registra una lista de transformaciones requeridas por el producto durante la instalación. El instalador debe aplicar estas transformaciones al paquete de instalación del producto al configurar o instalar el producto. Si una transformación enumerada no está disponible y la resistencia del origen de transformación no puede restaurarla, se produce un error en la instalación.

Una transformación puede modificar la información que se encuentra en cualquier tabla persistente de la base de [datos del instalador](installer-database.md). Una transformación también puede agregar o quitar tablas persistentes en la base de datos del instalador. Las transformaciones no pueden modificar ninguna parte de un paquete de instalación que no esté en una tabla de base de datos, como la información del flujo de información de [resumen,](summary-information-stream.md)la información de los subalmacenamientos o los archivos de los gabinetes incrustados.

Las transformaciones tienen un flujo de información de resumen que puede contener condiciones de validación y condiciones de error. Las condiciones de error y validación de transformación se pueden agregar a la información de resumen mediante la [**función MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) Las condiciones de validación controlan si el instalador puede aplicar la transformación a una base de datos de instalación determinada. La validación de la transformación puede estar condicionada a los valores de las propiedades [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) y [**ProductLanguage**](productlanguage.md) especificadas en la transformación y a los de la base de datos de instalación. Las condiciones de error de transformación controlan qué errores se suprimen cuando se aplica la transformación. Las condiciones de error incluidas en la transformación se reemplazan por las condiciones de error especificadas mediante los métodos [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) [**y ApplyTransform.**](database-applytransform.md)

> [!Note]  
> Las transformaciones de personalización típicas no tienen condiciones de validación ni se validan con [**ProductCode.**](productcode.md) Las transformaciones almacenadas en paquetes [de](patch-packages.md) revisión suelen tener condiciones de validación estrictas para asegurarse de que se aplica la transformación correcta al destino de revisión.

 

Hay tres tipos de transformaciones Windows Installer:

-   [Transformaciones insertadas](embedded-transforms.md)
-   [Transformaciones protegidas](secured-transforms.md)
-   [Transformaciones no seguras](unsecured-transforms.md)

 

 



