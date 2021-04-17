---
description: La propiedad UpgradeCode es un GUID que representa un conjunto de productos relacionado. El UpgradeCode se usa en la tabla de actualización para buscar las versiones relacionadas del producto que ya están instaladas. La acción RegisterProduct usa esta propiedad.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propiedad UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653631"
---
# <a name="upgradecode-property"></a>Propiedad UpgradeCode

La propiedad **UpgradeCode** es un GUID que representa un conjunto de productos relacionado. El **UpgradeCode** se usa en la [tabla de actualización](upgrade-table.md) para buscar las versiones relacionadas del producto que ya están instaladas.

La [acción RegisterProduct](registerproduct-action.md)usa esta propiedad.

## <a name="remarks"></a>Observaciones

Se recomienda encarecidamente que los autores de los paquetes de instalación especifiquen **UpgradeCode** para su aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[Preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




