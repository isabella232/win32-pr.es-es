---
description: La acción FindRelatedProducts se ejecuta a través de cada registro de la tabla de actualización en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Acción FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361032"
---
# <a name="findrelatedproducts-action"></a>Acción FindRelatedProducts

La acción FindRelatedProducts se ejecuta a través de cada registro de la [tabla de actualización](upgrade-table.md) en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema. Cuando FindRelatedProducts detecta una correspondencia entre la información de actualización y un producto instalado, anexa el código de producto a la propiedad especificada en la columna ActionProperty de UpgradeTable.

La acción FindRelatedProducts solo se ejecuta la primera vez que se instala el producto. La acción FindRelatedProducts no se ejecuta durante el modo de mantenimiento o la desinstalación.

## <a name="database-tables-queried"></a>Tablas de base de datos consultadas

Esta acción consulta la siguiente tabla:

[Actualizar tabla](upgrade-table.md)

## <a name="properties-used"></a>Propiedades usadas

La acción FindRelatedProducts usa la propiedad [**UpgradeCode**](upgradecode.md) y la información de versión e idioma que se creó en la tabla de actualización para detectar los productos instalados afectados por la actualización pendiente. Anexa el código de producto de los productos detectados a la propiedad en la columna ActionProperty de UpgradeTable.

FindRelatedProducts solo reconoce los productos existentes que se han instalado con el Windows Installer con un archivo. msi que define una propiedad [**UpgradeCode**](upgradecode.md) , una propiedad [**ProductVersion**](productversion.md) y un valor para la propiedad [**ProductLanguage**](productlanguage.md) que es uno de los idiomas enumerados en la propiedad Resumen de la [**plantilla**](template-summary.md) .

Tenga en cuenta que FindRelatedProducts usa el lenguaje devuelto por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Para que FindRelatedProducts funcione correctamente, el autor del paquete debe asegurarse de que la propiedad [**ProductLanguage**](productlanguage.md) de la [tabla de propiedades](property-table.md) esté establecida en un idioma que también aparezca en la propiedad Resumen de la [**plantilla**](template-summary.md) . Consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

FindRelatedProducts debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en las tablas [InstallExecuteSequence](installexecutesequence-table.md) . El instalador impide que los productos de FindRelated se ejecuten en InstallExecuteSequence si la acción ya se ejecutó en InstallUISequence. La acción FindRelatedProducts debe ser anterior a la [acción MigrateFeatureStates](migratefeaturestates-action.md) y la [acción RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

FindRelatedProducts envía un mensaje de datos de acción para cada producto relacionado que detecta en el sistema.

 

 



