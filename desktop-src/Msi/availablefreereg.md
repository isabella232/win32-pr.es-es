---
description: La propiedad AVAILABLEFREEREG especifica en kilobytes el espacio libre total disponible en el Registro después de llamar a la acción AllocateRegistrySpace. El valor máximo de la propiedad AVAILABLEFREEREG es 200 0000 kilobytes. Esta propiedad solo se establece en Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: AVAILABLEFREEREG, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650075"
---
# <a name="availablefreereg-property"></a>AVAILABLEFREEREG, propiedad

La **propiedad AVAILABLEFREEREG** especifica en kilobytes el espacio libre total disponible en el Registro después de llamar a la [acción AllocateRegistrySpace](allocateregistryspace-action.md).

El valor máximo de la **propiedad AVAILABLEFREEREG** es 200 0000 kilobytes.

Esta propiedad solo se establece en Windows 2000.

## <a name="remarks"></a>Comentarios

La **propiedad AVAILABLEFREEREG** debe establecerse en un valor lo suficientemente grande como para garantizar el espacio suficiente en el Registro para toda la información de registro agregada por la instalación. El valor mínimo necesario para garantizar que haya espacio suficiente depende de dónde se encuentra la acción [AllocateRegistrySpace](allocateregistryspace-action.md) en la secuencia de acciones porque el instalador aumenta automáticamente el espacio según sea necesario al registrar información en las tablas [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)y [Verb.](verb-table.md) El instalador no aumenta el espacio total del Registro a la cantidad especificada por **AVAILABLEFREEREG** hasta llegar a AllocateRegistrySpace en la secuencia de acción.

Si AllocateRegistrySpace es una de las primeras acciones de la secuencia de acciones, **AVAILABLEFREEREG** debe establecerse en el espacio total requerido por la información de registro en la tabla del Registro, la tabla Class, la tabla TypeLib, la tabla SelfReg, la tabla Extension, la tabla MIME, la tabla [Verb,](custom-actions.md) el registro de acciones personalizadas, el registro propio y cualquier otra información del Registro escrita durante la instalación. El valor **de AVAILABLEFREEREG es** la cantidad total de información agregada por la instalación y garantiza espacio suficiente en todos los casos. Este también es el caso más común.

Si la acción AllocateRegistrySpace se puede crear [](standard-actions.md) en la secuencia de acciones después de todas las acciones estándar que escriben datos de registro, como [WriteRegistryValues](writeregistryvalues-action.md) y [RegisterClassInfo](registerclassinfo-action.md), el valor de **AVAILABLEFREEREG** solo debe establecerse en el espacio necesario para registrar acciones personalizadas, registrar bibliotecas de tipos y cualquier otra información que aún no se haya registrado a través de las tablas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




