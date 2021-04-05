---
description: UpgradeCode se utiliza principalmente para admitir las actualizaciones principales, aunque las revisiones de actualización pequeñas y secundarias pueden usar UpgradeCode para la validación del producto.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Usar UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf32d40364653527b9f906e6dd42de64bb9f697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908998"
---
# <a name="using-an-upgradecode"></a>Usar UpgradeCode

[**UpgradeCode**](upgradecode.md) se utiliza principalmente para admitir las actualizaciones principales, aunque las revisiones de actualización pequeñas y secundarias pueden usar **UpgradeCode** para la validación del producto. Durante las actualizaciones principales, las acciones [FindRelatedProducts](findrelatedproducts-action.md), [MigrateFeatureStates](migratefeaturestates-action.md)y [RemoveExistingProducts](removeexistingproducts-action.md) detectan, migran y quitan versiones anteriores del producto. La acción FindRelatedProducts busca productos mediante criterios basados en **UpgradeCode**, [**ProductLanguage**](productlanguage.md)y [**ProductVersion**](productversion.md). Estos criterios se especifican en la tabla de [actualización](upgrade-table.md) .

Dados los criterios usados por la acción [FindRelatedProducts](findrelatedproducts-action.md) , [**UpgradeCode**](upgradecode.md) puede ser el mismo para diferentes idiomas y versiones de un único producto. Esto se debe a que la tabla de [actualización](upgrade-table.md) permite diferenciar entre productos a lo largo de la versión y las líneas de idioma.

En las distintas versiones del mismo producto, puede que nunca necesite cambiar [**UpgradeCode**](upgradecode.md). Cada producto independiente debe tener su propio **UpgradeCode**. Un conjunto de productos también debe tener su propio **UpgradeCode**. Si lo hace, permitirá que el conjunto actualice versiones anteriores del conjunto o productos independientes mediante el uso de varias filas en la [tabla de actualización](upgrade-table.md).

Los dos escenarios siguientes muestran el uso de [**UpgradeCode**](upgradecode.md).

-   El producto A y el producto B se enviaron con las mismas [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md)y [**UpgradeCode**](upgradecode.md). Los productos A y B tienen diferentes [**ProductCodes**](productcode.md). Dado que a los productos se les ha asignado el mismo **UpgradeCode**, no se puede crear la tabla de [actualización](upgrade-table.md) para diferenciar la versión anterior del producto a de la versión anterior del producto B. En este caso, no podrá tener una instalación de actualización del producto A que omita el producto B. Dado que se trata de productos diferentes, deben tener asignado un **UpgradeCode** diferente.
-   Las versiones en inglés y en francés del producto A se enviaron con los mismos [**ProductVersion**](productversion.md) y [**UpgradeCode**](upgradecode.md). Las versiones en inglés y en francés del producto A tienen [**ProductLanguages**](productlanguage.md) y [**ProductCodes**](productcode.md)diferentes. Aunque las versiones en inglés y en francés comparten el mismo **UpgradeCode**, es posible crear la tabla de [actualización](upgrade-table.md) de modo que solo se detecte y actualice la versión anterior del idioma inglés y se omita la versión anterior en francés. Diferentes versiones de idioma de un producto pueden utilizar el mismo **UpgradeCode**.

 

 



