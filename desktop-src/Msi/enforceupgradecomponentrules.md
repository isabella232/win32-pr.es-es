---
description: Se trata de una directiva del sistema por equipo que se puede usar para aplicar reglas de componentes de actualización durante pequeñas actualizaciones y actualizaciones secundarias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002145"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Se trata de una [Directiva del sistema](system-policy.md) por equipo que se puede usar para aplicar reglas de componentes de actualización durante [pequeñas actualizaciones](small-updates.md) y actualizaciones [secundarias](minor-upgrades.md).

Establezca la Directiva EnforceUpgradeComponentRules en 1 para aplicar las reglas de componentes de actualización durante [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) de todos los productos del equipo. Para aplicar las reglas durante las actualizaciones pequeñas y las actualizaciones secundarias de un producto determinado, establezca la propiedad [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) en 1 en la línea de comandos o en la [tabla de propiedades](property-table.md).

Cuando la propiedad o la Directiva se han establecido en 1, se puede producir un error en [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) porque la actualización intenta hacer lo siguiente:

-   Agregue una nueva característica a la parte superior o central de un árbol de características existente.

    La nueva característica debe agregarse como una nueva característica hoja a un árbol de características existente.

    En este caso, se puede cambiar el [**ProductCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal](major-upgrades.md).

-   Quitar un componente de una característica.

    Esto también puede ocurrir si cambia el GUID de un componente. El componente identificado por el GUID original parece quitarse y el componente identificado por el nuevo GUID aparece como un nuevo componente.

    **Windows Installer 4,5 y versiones posteriores:** El componente se puede quitar correctamente mediante Windows Installer 4,5 o posterior estableciendo el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md) o estableciendo la propiedad [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    Como alternativa, se puede cambiar el [**ProductCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal](major-upgrades.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



