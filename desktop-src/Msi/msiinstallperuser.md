---
description: El usuario puede establecer las propiedades MSIINSTALLPERUSER y ALLUSERS en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el instalador de Windows instale un paquete de doble propósito para el usuario actual o para todos los usuarios del equipo.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: MsiINSTALLPERUSER, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071846"
---
# <a name="msiinstallperuser-property"></a>MsiINSTALLPERUSER, propiedad

El usuario puede establecer las propiedades **MSIINSTALLPERUSER** y [**ALLUSERS**](allusers.md) en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el instalador de Windows instale un paquete de doble propósito para el usuario actual o para todos los usuarios del equipo. Para usar la propiedad **MSIINSTALLPERUSER,** el valor de la propiedad [**ALLUSERS**](allusers.md) debe ser 2 y el paquete debe haber sido autor de la instalación en el contexto por usuario o por equipo. Para obtener información sobre cómo crear un paquete de doble propósito, vea [Single Package Authoring](single-package-authoring.md). Si el valor de la **propiedad ALLUSERS** no es igual a 2, el valor de la propiedad **MSIINSTALLPERUSER** se omite y no tiene ningún efecto en la instalación. El valor de **la propiedad MSIINSTALLPERUSER** se omite al instalar el paquete mediante Windows Installer 4.5 o versiones anteriores.

Para solicitar que el instalador de Windows instale el paquete de doble propósito en el contexto de instalación por equipo [,](installation-context.md)el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en una cadena vacía ("") y el valor de la propiedad [**ALLUSERS**](allusers.md) en 2 mediante una interfaz de usuario o una línea de comandos.

Para solicitar que el instalador de Windows instale el paquete de doble propósito en el contexto de instalación por usuario [,](installation-context.md)el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en 1 y el valor de la propiedad [**ALLUSERS**](allusers.md) en 2 mediante una interfaz de usuario o una línea de comandos.

Si el valor de la [**propiedad ALLUSERS**](allusers.md) no es igual a 2, Windows Installer omite el valor de la **propiedad MSIINSTALLPERUSER.** Si Windows instalador instala la aplicación en el contexto por equipo, restablece el valor de la **propiedad ALLUSERS** a 1. Si Windows Installer instala la aplicación en el contexto por usuario, restablece el valor de la propiedad **ALLUSERS** a una cadena vacía (""). Por lo tanto, las aplicaciones que se han instalado por usuario reciben todas las actualizaciones o reparaciones por usuario y las aplicaciones instaladas por equipo reciben actualizaciones o reparaciones por equipo.

**[Windows Installer 4.5](not-supported-in-windows-installer-4-5.md)** o versiones anteriores: las versiones anteriores a Windows Installer 5.0 omiten la propiedad **MSIINSTALLPERUSER.**

## <a name="default-value"></a>Valor predeterminado

El contexto de instalación predeterminado recomendado es por usuario para un paquete de doble propósito. Cree MSIINSTALLPERUSER=1 y ALLUSERS=2 en la tabla [Property](property-table.md) del paquete de doble propósito para especificar por usuario como contexto de instalación predeterminado.

## <a name="remarks"></a>Observaciones

Para asegurarse de que no se ha establecido la propiedad **MSIINSTALLPERUSER,** establezca su valor en una cadena vacía (""), MSIINSTALLPERUSER="".

El contexto de instalación determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder,**](admintoolsfolder.md) [**ProgramFilesFolder,**](programfilesfolder.md) [**CommonFilesFolder,**](commonfilesfolder.md) [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder.**](commonfiles64folder.md) El contexto de instalación determina las partes del [](registry-table.md) Registro donde se escriben o quitan las entradas de la tabla Registry y [removeRegistry](removeregistry-table.md), con -1 en la columna Raíz. Para obtener información sobre el contexto de instalación, vea [Contexto de instalación](installation-context.md)de .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Contexto de instalación](installation-context.md)
</dt> <dt>

[Creación de paquete único](single-package-authoring.md)
</dt> </dl>

 

 




