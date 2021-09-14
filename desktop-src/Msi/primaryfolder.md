---
description: PRIMARYFOLDER es una propiedad global que permite al autor designar una carpeta principal para la instalación.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propiedad PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161451"
---
# <a name="primaryfolder-property"></a>Propiedad PRIMARYFOLDER

**PRIMARYFOLDER es** una propiedad global que permite al autor designar una carpeta principal para la instalación. El valor de esta propiedad debe ser el nombre de clave de un directorio que exista en la [tabla Directory](directory-table.md).

El instalador usa la ruta de acceso resuelta de la carpeta principal para determinar qué volumen se va a usar al establecer los valores de la propiedad [**PrimaryVolumePath,**](primaryvolumepath.md) [**primaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) la propiedad [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) y la propiedad [**PrimaryVolumeSpaceRemaining.**](primaryvolumespaceremaining.md) El instalador proporciona los valores de estas últimas propiedades a los usuarios de la interfaz de usuario para ayudarles a administrar el espacio en disco. Normalmente, los autores de paquetes pueden seleccionar la carpeta más grande como carpeta principal.

El valor de esta propiedad debe ser el nombre de clave de un registro de directorio que se encuentra en la [tabla Directory](directory-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




