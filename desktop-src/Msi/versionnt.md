---
description: El instalador establece la propiedad VersionNT en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propiedad VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f2787f7b4914495bc257629e7b50765d7e93ec221cf1aa44d9c1f7e706d127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995645"
---
# <a name="versionnt-property"></a>Propiedad VersionNT

El instalador establece la propiedad **VersionNT** en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7. El valor es un entero: MajorVersion \* 100 + MinorVersion.

Las instrucciones condicionales que dependen del sistema operativo pueden usar esta propiedad.

Vea también [Valores de propiedad del sistema operativo](operating-system-property-values.md).

## <a name="remarks"></a>Comentarios

Las expresiones de condición pueden probar Windows NT, Windows 2000 o Windows XP mediante el nombre de propiedad o pueden comprobar la versión mediante un operador de comparación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP Consulte los requisitos de Run-Time del instalador de [Windows](windows-installer-portal.md) para obtener información sobre el service pack de Windows mínimo que requiere una versión del instalador de Windows.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




