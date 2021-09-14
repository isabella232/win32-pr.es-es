---
description: La acción FindRelatedProducts se ejecuta a través de cada registro de la tabla Upgrade en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Acción FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074776"
---
# <a name="findrelatedproducts-action"></a>Acción FindRelatedProducts

La acción FindRelatedProducts se ejecuta a través de cada registro de la tabla [Upgrade](upgrade-table.md) en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema. Cuando FindRelatedProducts detecta una correspondencia entre la información de actualización y un producto instalado, anexa el código de producto a la propiedad especificada en la columna ActionProperty de UpgradeTable.

La acción FindRelatedProducts solo se ejecuta la primera vez que se instala el producto. La acción FindRelatedProducts no se ejecuta durante el modo de mantenimiento o la desinstalación.

## <a name="database-tables-queried"></a>Tablas de base de datos consultadas

Esta acción consulta la tabla siguiente:

[Actualizar tabla](upgrade-table.md)

## <a name="properties-used"></a>Propiedades usadas

La acción FindRelatedProducts usa la propiedad [**UpgradeCode**](upgradecode.md) y la información de versión e idioma que se ha creado en la tabla Upgrade para detectar los productos instalados afectados por la actualización pendiente. Anexa el código de producto de los productos detectados a la propiedad de la columna ActionProperty de UpgradeTable.

FindRelatedProducts solo reconoce los productos existentes que se han instalado mediante el instalador de Windows con un .msi que define una propiedad [**UpgradeCode,**](upgradecode.md) una propiedad [**ProductVersion**](productversion.md) y un valor para la propiedad [**ProductLanguage**](productlanguage.md) que es uno de los idiomas enumerados en la propiedad [**Resumen**](template-summary.md) de plantilla.

Tenga en cuenta que FindRelatedProducts usa el lenguaje devuelto [**por MsiGetProductInfo.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) Para que FindRelatedProducts funcione correctamente, el autor del paquete debe asegurarse de que la propiedad [**ProductLanguage**](productlanguage.md) de la tabla [Property](property-table.md) está establecida en un idioma que también aparece en la propiedad [**Resumen**](template-summary.md) de plantilla. Consulte [Preparar una aplicación para futuras actualizaciones principales.](preparing-an-application-for-future-major-upgrades.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

FindRelatedProducts debe crearse en las tablas [InstallUISequence](installuisequence-table.md) e [InstallExecuteSequence.](installexecutesequence-table.md) El instalador impide que FindRelated Products se ejecute en InstallExecuteSequence si la acción ya se ha ejecutado en InstallUISequence. La acción FindRelatedProducts debe ir antes [de la acción MigrateFeatureStates](migratefeaturestates-action.md) y [la acción RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

FindRelatedProducts envía un mensaje de datos de acción para cada producto relacionado que detecta en el sistema.

 

 



