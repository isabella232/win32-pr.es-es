---
description: El instalador establece la propiedad WindowsVolume en el volumen de la carpeta windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propiedad WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063013"
---
# <a name="windowsvolume-property"></a>Propiedad WindowsVolume

El instalador establece la **propiedad WindowsVolume** en el volumen de la carpeta windows. La propiedad siempre termina con una barra diagonal inversa. Esto se puede usar para establecer la ubicación predeterminada en el volumen en el que se encuentra la carpeta Windows porque la [**propiedad ROOTDRIVE**](rootdrive.md) no es necesariamente igual a esta unidad.

## <a name="remarks"></a>Observaciones

No use la **propiedad WindowsVolume** en la columna Directory de la [tabla Directory.](directory-table.md) La [**propiedad WindowsFolder**](windowsfolder.md) contiene la ruta de acceso a Windows carpeta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP Consulte los requisitos de Run-Time del instalador de [Windows](windows-installer-portal.md) para obtener información sobre el Service Pack de Windows mínimo que requiere una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




