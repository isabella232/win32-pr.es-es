---
description: UpgradeCode se usa principalmente para admitir actualizaciones principales, aunque las revisiones de actualización pequeñas y secundarias pueden usar UpgradeCode para la validación del producto.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Uso de upgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482bdaa228bc57432ab730e59f265fc50352c3a63ed29f75ee0a63c65c201ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039095"
---
# <a name="using-an-upgradecode"></a>Uso de upgradeCode

[**UpgradeCode se**](upgradecode.md) usa principalmente para admitir actualizaciones principales, aunque las revisiones de actualización pequeñas y secundarias pueden usar **UpgradeCode** para la validación del producto. Durante las actualizaciones principales, las acciones [FindRelatedProducts,](findrelatedproducts-action.md) [MigrateFeatureStates](migratefeaturestates-action.md)y [RemoveExistingProducts](removeexistingproducts-action.md) detectan, migran y quitan versiones anteriores del producto. La acción FindRelatedProducts busca productos que usan criterios basados en **UpgradeCode,** [**ProductLanguage**](productlanguage.md)y [**ProductVersion.**](productversion.md) Estos criterios se especifican en la [tabla Upgrade.](upgrade-table.md)

Dados los criterios utilizados por [la acción FindRelatedProducts,](findrelatedproducts-action.md) [**UpgradeCode**](upgradecode.md) puede ser el mismo para distintos idiomas y versiones de un único producto. Esto se debe a que [la tabla Upgrade](upgrade-table.md) permite diferenciar entre productos a lo largo de las líneas de versión y idioma.

En distintas versiones del mismo producto, es posible que nunca tenga que cambiar [**upgradeCode**](upgradecode.md). Cada producto independiente debe tener su propio **UpgradeCode.** Un conjunto de productos también debe tener su **propio UpgradeCode.** Al hacerlo, el conjunto de aplicaciones podrá actualizar versiones anteriores del conjunto de aplicaciones o productos independientes mediante el uso de varias filas en la [tabla Actualizar](upgrade-table.md).

Los dos escenarios siguientes ilustran el uso de [**UpgradeCode**](upgradecode.md).

-   Los productos A y B se enviaron con los mismos [**ProductLanguage,**](productlanguage.md) [**ProductVersion**](productversion.md)y [**UpgradeCode.**](upgradecode.md) Los productos A y B tienen [**distintos productcodes.**](productcode.md) Dado que a los productos se [](upgrade-table.md) les asignó el mismo **UpgradeCode,** no se puede crear la tabla Upgrade para diferenciar la versión anterior del Producto A de la versión anterior del Producto B. En este caso, no podrá tener una instalación de actualización del Producto A que ignore el Producto B. Dado que se trata de productos diferentes, cada uno de ellos debe tener asignado un **upgradeCode diferente.**
-   Las versiones en inglés y francés del producto A se enviaron con los mismos [**ProductVersion**](productversion.md) y [**UpgradeCode.**](upgradecode.md) Las versiones en inglés y francés del producto A tienen [**diferentes ProductLanguages**](productlanguage.md) y [**ProductCodes.**](productcode.md) Aunque las versiones en inglés y francés comparten el mismo [](upgrade-table.md) **UpgradeCode,** es posible crear la tabla Upgrade de forma que solo se detecte y actualice la versión anterior del idioma inglés y se ignore la versión anterior del francés. Las distintas versiones de idioma de un producto pueden usar el mismo **upgradeCode**.

 

 



