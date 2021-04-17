---
description: La propiedad TARGETDIR especifica el directorio de destino raíz de la instalación.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propiedad TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680527"
---
# <a name="targetdir-property"></a>Propiedad TARGETDIR

La propiedad **targetDir** especifica el directorio de destino raíz de la instalación. **TargetDir** debe ser el nombre de una raíz en la tabla del [directorio](directory-table.md) . Puede haber un único directorio de destino raíz. Durante una [instalación administrativa](administrative-installation.md) , esta propiedad especifica la ubicación en la que se va a copiar el paquete de instalación. Durante una instalación no administrativa, esta propiedad especifica el directorio de destino raíz.

Para especificar el directorio raíz de destino, establezca la columna directorio de la tabla directorio en la propiedad **targetDir** y la columna DefaultDir en la propiedad [**SourceDir**](sourcedir.md) . Si se define la propiedad **targetDir** , el directorio de destino se resuelve en el valor de la propiedad. Si la propiedad **targetDir** es undefined, la propiedad [**ROOTDRIVE**](rootdrive.md) se utiliza para resolver la ruta de acceso. Para obtener más información sobre el uso de la propiedad **targetDir** , vea [usar la tabla de directorio](using-the-directory-table.md).

Tenga en cuenta que el valor de la propiedad **targetDir** se establece normalmente en la línea de comandos o a través de una interfaz de usuario. No se recomienda establecer **targetDir** mediante la creación de una ruta de acceso en la [tabla de propiedades](property-table.md) porque los equipos difieren en la configuración de la unidad local.

Para obtener más información sobre cómo cambiar el TARGETDIR durante una instalación, consulte [cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




