---
description: La propiedad UpgradeCode es un GUID que representa un conjunto relacionado de productos. UpgradeCode se usa en la tabla de actualización para buscar versiones relacionadas del producto que ya están instaladas. La acción RegisterProduct usa esta propiedad.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propiedad UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e42253dfe0466636783603f6b5098425503a9f0984363e11d4c7241b17a191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809665"
---
# <a name="upgradecode-property"></a>Propiedad UpgradeCode

La **propiedad UpgradeCode** es un GUID que representa un conjunto relacionado de productos. UpgradeCode **se** usa en la [tabla de actualización](upgrade-table.md) para buscar versiones relacionadas del producto que ya están instaladas.

La acción [RegisterProduct](registerproduct-action.md)usa esta propiedad .

## <a name="remarks"></a>Comentarios

Se recomienda encarecidamente que los autores de paquetes de instalación especifiquen **un upgradeCode** para su aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Aplicación de revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[Preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




