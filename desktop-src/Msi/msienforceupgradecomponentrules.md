---
description: Establezca la propiedad MSIENFORCEUPGRADECOMPONENTRULES en 1 en la línea de comandos o en la tabla Property para aplicar las reglas del componente de actualización durante pequeñas actualizaciones y actualizaciones secundarias de un producto determinado.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propiedad MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071861"
---
# <a name="msienforceupgradecomponentrules-property"></a>Propiedad MSIENFORCEUPGRADECOMPONENTRULES

Establezca la **propiedad MSIENFORCEUPGRADECOMPONENTRULES** en 1 en la línea de comandos [](small-updates.md) o en la tabla [Property](property-table.md) para aplicar las reglas del componente de actualización durante pequeñas actualizaciones y actualizaciones [secundarias](minor-upgrades.md) de un producto determinado. Para aplicar las reglas durante pequeñas actualizaciones y actualizaciones secundarias de todos los productos del equipo, establezca la directiva [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) en 1.

Cuando la propiedad o directiva se [](small-updates.md) establece en 1, se pueden producir errores en las actualizaciones pequeñas y [secundarias](minor-upgrades.md) porque la actualización intenta hacer lo siguiente que infringe las reglas del componente de actualización:

-   Agregue una nueva característica a la parte superior o central de un árbol de características existente.

    La nueva característica debe agregarse como una nueva característica hoja a un árbol de características existente.

    En este caso, se [**puede cambiar el productCode**](productcode.md) del producto y la actualización se puede tratar como una [actualización principal.](major-upgrades.md)

-   Quitar un componente de una característica.

    Esto también puede ocurrir si cambia el GUID de un componente. El componente identificado por el GUID original parece quitarse y el componente identificado por el nuevo GUID aparece como un nuevo componente.

    **Windows Installer 4.5 y versiones posteriores:** El componente se puede quitar correctamente mediante Windows Installer 4.5 y versiones posteriores estableciendo el atributo [](component-table.md) **msidbComponentAttributesUninstallOnSupersedence** en la tabla de componentes o estableciendo la propiedad [**MSIUNINSTALLSUPERSEDCOMPONENTS.**](msiuninstallsupersededcomponents.md)

    Como alternativa, se [**puede cambiar el productCode**](productcode.md) del producto y la actualización se puede tratar como una [actualización principal.](major-upgrades.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




