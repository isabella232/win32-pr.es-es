---
description: El instalador establece la propiedad VersionNT en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propiedad VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653670"
---
# <a name="versionnt-property"></a>Propiedad VersionNT

El instalador establece la propiedad **VersionNT** en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 o Windows 7. El valor es un entero: MajorVersion \* 100 + MinorVersion.

Las instrucciones condicionales que dependen del sistema operativo pueden utilizar esta propiedad.

Vea también [valores de propiedad del sistema operativo](operating-system-property-values.md).

## <a name="remarks"></a>Observaciones

Las expresiones de condición pueden probar Windows NT, Windows 2000 o Windows XP con el nombre de la propiedad, o puede comprobar la versión mediante un operador de comparación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP, consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows necesaria para una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




