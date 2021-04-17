---
description: El instalador establece la propiedad WindowsVolume en el volumen de la carpeta Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propiedad WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653668"
---
# <a name="windowsvolume-property"></a>Propiedad WindowsVolume

El instalador establece la propiedad **WindowsVolume** en el volumen de la carpeta Windows. La propiedad siempre termina con una barra diagonal inversa. Se puede usar para establecer la ubicación predeterminada en el volumen en el que se encuentra la carpeta de Windows, ya que la propiedad [**ROOTDRIVE**](rootdrive.md) no es necesariamente igual a esta unidad.

## <a name="remarks"></a>Observaciones

No use la propiedad **WindowsVolume** en la columna directorio de la tabla [directorio](directory-table.md) . La propiedad [**WindowsFolder**](windowsfolder.md) contiene la ruta de acceso a la carpeta de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP, consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows necesaria para una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




