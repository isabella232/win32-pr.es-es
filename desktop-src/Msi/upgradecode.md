---
description: La propiedad UpgradeCode es un GUID que representa un conjunto relacionado de productos. UpgradeCode se usa en la tabla de actualización para buscar versiones relacionadas del producto que ya están instaladas. La acción RegisterProduct usa esta propiedad.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propiedad UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254103"
---
# <a name="upgradecode-property"></a>Propiedad UpgradeCode

La **propiedad UpgradeCode** es un GUID que representa un conjunto relacionado de productos. UpgradeCode **se** usa en la [tabla de actualización](upgrade-table.md) para buscar versiones relacionadas del producto que ya están instaladas.

La acción [RegisterProduct](registerproduct-action.md)usa esta propiedad .

## <a name="remarks"></a>Observaciones

Se recomienda encarecidamente que los autores de paquetes de instalación especifiquen **un upgradeCode** para su aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Aplicación de revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[Preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




