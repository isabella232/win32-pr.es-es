---
description: El usuario puede establecer las propiedades MSIINSTALLPERUSER y ALLUSERS en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el Windows Installer instalar un paquete de doble finalidad para el usuario actual o para todos los usuarios del equipo.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propiedad MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653391"
---
# <a name="msiinstallperuser-property"></a>Propiedad MSIINSTALLPERUSER

El usuario puede establecer las propiedades **MSIINSTALLPERUSER** y [**AllUsers**](allusers.md) en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el Windows Installer instalar un paquete de doble finalidad para el usuario actual o para todos los usuarios del equipo. Para usar la propiedad **MSIINSTALLPERUSER** , el valor de la propiedad [**AllUsers**](allusers.md) debe ser 2 y se debe haber creado el paquete para poder instalarlo en el contexto por usuario o por equipo. Para obtener información sobre la creación de un paquete de doble propósito, vea creación de un [solo paquete](single-package-authoring.md). Si el valor de la propiedad **AllUsers** no es igual a 2, el valor de la propiedad **MSIINSTALLPERUSER** se omite y no tiene ningún efecto en la instalación. El valor de la propiedad **MSIINSTALLPERUSER** se omite al instalar el paquete con Windows Installer 4,5 o una versión anterior.

Para solicitar que el Windows Installer instalar el paquete de uso dual en el [contexto de instalación](installation-context.md)por máquina, el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en una cadena vacía ("") y el valor de la propiedad [**AllUsers**](allusers.md) en 2 mediante una interfaz de usuario creada o una línea de comandos.

Para solicitar que el Windows Installer instalar el paquete de uso dual en el [contexto de instalación](installation-context.md)por usuario, el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en 1 y el valor de la propiedad [**AllUsers**](allusers.md) en 2 mediante una interfaz de usuario creada o una línea de comandos.

Si el valor de la propiedad [**AllUsers**](allusers.md) no es igual a 2, el Windows Installer omite el valor de la propiedad **MSIINSTALLPERUSER** . Si Windows Installer instala la aplicación en el contexto por equipo, restablece el valor de la propiedad **AllUsers** en 1. Si Windows Installer instala la aplicación en el contexto por usuario, restablece el valor de la propiedad **AllUsers** en una cadena vacía (""). Por lo tanto, las aplicaciones que se han instalado por usuario reciben todas las actualizaciones o reparaciones por usuario y las aplicaciones instaladas por máquina reciben actualizaciones o reparaciones por equipo.

**[Windows Installer 4,5 o anterior](not-supported-in-windows-installer-4-5.md):** las versiones anteriores a Windows Installer 5,0 omiten la propiedad **MSIINSTALLPERUSER** .

## <a name="default-value"></a>Valor predeterminado

El contexto de instalación predeterminado recomendado es por usuario para un paquete de doble finalidad. Author MSIINSTALLPERUSER = 1 y ALLUSERS = 2 en la [tabla de propiedades](property-table.md) del paquete de doble uso para especificar por usuario como el contexto de instalación predeterminado.

## <a name="remarks"></a>Observaciones

Puede asegurarse de que la propiedad **MSIINSTALLPERUSER** no se ha establecido estableciendo su valor en una cadena vacía (""), MSIINSTALLPERUSER = "".

El contexto de instalación determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder**](commonfiles64folder.md) . El contexto de instalación determina las partes del registro en las que se escriben o se quitan las entradas de la tabla [del registro](registry-table.md) y la [tabla RemoveRegistry](removeregistry-table.md), con-1 en la columna raíz. Para obtener información sobre el contexto de instalación, vea [contexto de instalación](installation-context.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Contexto de instalación](installation-context.md)
</dt> <dt>

[Creación de un solo paquete](single-package-authoring.md)
</dt> </dl>

 

 




