---
description: Se trata de una directiva de sistema por máquina que se puede usar para aplicar reglas de componentes de actualización durante actualizaciones pequeñas y actualizaciones secundarias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158483"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Se trata de una directiva de [sistema por](system-policy.md) equipo que se puede usar para aplicar reglas de componentes de actualización durante actualizaciones [pequeñas](small-updates.md) y [actualizaciones secundarias.](minor-upgrades.md)

Establezca la directiva EnforceUpgradeComponentRules en 1 [](small-updates.md) para aplicar reglas de componentes de actualización durante pequeñas actualizaciones y actualizaciones [secundarias](minor-upgrades.md) de todos los productos del equipo. Para aplicar las reglas durante pequeñas actualizaciones y actualizaciones secundarias de un producto determinado, establezca la propiedad [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) en 1 en la línea de comandos o en la [tabla Property](property-table.md).

Cuando la propiedad o directiva se [](small-updates.md) ha establecido en 1, se pueden producir errores en las actualizaciones pequeñas y [secundarias](minor-upgrades.md) porque la actualización intenta hacer lo siguiente:

-   Agregue una nueva característica a la parte superior o central de un árbol de características existente.

    La nueva característica debe agregarse como una nueva característica hoja a un árbol de características existente.

    En este caso, se puede cambiar [**el productCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal.](major-upgrades.md)

-   Quitar un componente de una característica.

    Esto también puede ocurrir si cambia el GUID de un componente. El componente identificado por el GUID original parece quitarse y el componente identificado por el nuevo GUID aparece como un nuevo componente.

    **Windows Installer 4.5 y versiones posteriores:** El componente se puede quitar correctamente mediante Windows Installer 4.5 o posterior estableciendo el atributo **msidbComponentAttributesUninstallOnSupersedence** en la tabla [Component](component-table.md) o estableciendo la propiedad [**MSIUNINSTALLSUPERSEDCOMPONENTS.**](msiuninstallsupersededcomponents.md)

    Como alternativa, se [**puede cambiar el productCode**](productcode.md) del producto y las actualizaciones se pueden tratar como una [actualización principal.](major-upgrades.md)

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



