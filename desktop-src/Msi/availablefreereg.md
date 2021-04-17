---
description: La propiedad AVAILABLEFREEREG especifica en kilobytes el espacio libre total disponible en el registro después de llamar a la acción AllocateRegistrySpace. El valor máximo de la propiedad AVAILABLEFREEREG es 2 millones kilobytes. Esta propiedad se establece únicamente en Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propiedad AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653817"
---
# <a name="availablefreereg-property"></a>Propiedad AVAILABLEFREEREG

La propiedad **AVAILABLEFREEREG** especifica en kilobytes el espacio libre total disponible en el registro después de llamar a la [acción AllocateRegistrySpace](allocateregistryspace-action.md).

El valor máximo de la propiedad **AVAILABLEFREEREG** es 2 millones kilobytes.

Esta propiedad se establece únicamente en Windows 2000.

## <a name="remarks"></a>Observaciones

La propiedad **AVAILABLEFREEREG** debe establecerse en un valor lo suficientemente grande como para garantizar espacio suficiente en el registro para toda la información de registro agregada por la instalación. El valor mínimo necesario para garantizar que el espacio sea suficiente depende de dónde se encuentre la [acción AllocateRegistrySpace](allocateregistryspace-action.md) en la secuencia de acción porque el instalador aumenta automáticamente el espacio según sea necesario al registrar la información en las tablas [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)y [Verb](verb-table.md) . El instalador no aumenta el espacio total del registro hasta la cantidad especificada por **AVAILABLEFREEREG** hasta llegar a AllocateRegistrySpace en la secuencia de acción.

Si AllocateRegistrySpace es una de las primeras acciones de la secuencia de acciones, **AVAILABLEFREEREG** debe establecerse en el espacio total requerido por la información de registro en la tabla del registro, la tabla de clases, la tabla typelib, la tabla SelfReg, la tabla de extensión, la tabla MIME, la tabla de verbos, el registro de [acciones personalizadas](custom-actions.md) , el registro propio y cualquier otra información del registro escrita durante la instalación El valor de **AVAILABLEFREEREG** es la cantidad total de información agregada por la instalación y garantiza suficiente espacio en todos los casos. Este es también el caso más común.

Si la acción AllocateRegistrySpace se puede crear en la secuencia de acciones después de todas [las acciones estándar](standard-actions.md) que escriben los datos de registro, como [WriteRegistryValues](writeregistryvalues-action.md) y [RegisterClassInfo](registerclassinfo-action.md), el valor de **AVAILABLEFREEREG** solo debe establecerse en el espacio necesario para registrar las acciones personalizadas, registrar bibliotecas de tipos y cualquier otra información que no se haya registrado a través de las tablas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




