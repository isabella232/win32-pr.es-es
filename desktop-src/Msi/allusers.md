---
Description: La propiedad ALLUSERS configura el contexto de instalación del paquete.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Propiedad ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671455"
---
# <a name="allusers-property"></a>Propiedad ALLUSERS

La propiedad **AllUsers** configura el contexto de instalación del paquete. El Windows Installer realiza una instalación por usuario o una instalación por equipo en función de los privilegios de acceso del usuario, independientemente de que se requieran privilegios elevados para instalar la aplicación, el valor de la propiedad **AllUsers** , el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) y la versión del sistema operativo.

El valor de la propiedad **AllUsers** , en el momento de la instalación, determina el [contexto de instalación](installation-context.md).

-   El valor 1 de la propiedad **AllUsers** especifica el contexto de instalación por máquina.
-   Un valor de propiedad **AllUsers** de una cadena vacía ("") especifica el contexto de instalación por usuario.
-   Si el valor de la propiedad **AllUsers** está establecido en 2, el Windows Installer restablece siempre el valor de la propiedad **AllUsers** en 1 y realiza una instalación por equipo o restablece el valor de la propiedad **AllUsers** en una cadena vacía ("") y realiza una instalación por usuario. El valor ALLUSERS = 2 permite al sistema restablecer el valor de **AllUsers** y el contexto de instalación, en función de los privilegios del usuario y de la versión de Windows.

    **Windows 7:** Establezca la propiedad **AllUsers** en 2 para usar la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) para especificar el contexto de instalación. Establezca la propiedad **MSIINSTALLPERUSER** en una cadena vacía ("") para una instalación por equipo. Establezca la propiedad **MSIINSTALLPERUSER** en 1 para una instalación por usuario. Si el paquete se ha escrito siguiendo las instrucciones de desarrollo descritas en [creación de un solo paquete](single-package-authoring.md), los usuarios que tengan acceso de usuario podrán instalar en el contexto por usuario sin tener que proporcionar credenciales de UAC. Si el usuario tiene privilegios de acceso de usuario, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo de UAC.

    **Windows Vista:** Establezca la propiedad **AllUsers** en 2 y Windows Installer cumpla con el [*control de cuentas de usuario*](u-gly.md) (UAC). Si el usuario tiene privilegios de acceso de usuario y ALLUSERS = 2, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo de UAC. Si UAC está habilitado y no se proporcionan las credenciales de administrador correctas, se produce un error en la instalación y se indica que se requieren privilegios de administrador. Si UAC está deshabilitado por la clave del registro, la Directiva de grupo o el panel de control, no se muestra el cuadro de diálogo UAC y se produce un error en la instalación con un error que indica que se requieren privilegios de administrador.

    **Windows XP:** Establezca la propiedad **AllUsers** en 2 y Windows Installer realiza una instalación por usuario si el usuario tiene privilegios de acceso de usuario.

-   Si el valor de la propiedad **AllUsers** no es igual a 2, el Windows Installer omite el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) .

## <a name="example"></a>Ejemplo

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) en github.

## <a name="default-value"></a>Valor predeterminado

El contexto de instalación predeterminado recomendado es por usuario. Si no se establece **AllUsers** , el instalador realiza una instalación por usuario. Puede asegurarse de que la propiedad **AllUsers** no se ha establecido estableciendo su valor en una cadena vacía (""), AllUsers = "".

## <a name="remarks"></a>Observaciones

El [contexto de instalación](installation-context.md) determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder**](commonfiles64folder.md) . El contexto de instalación determina las partes del registro en las que se escriben o se quitan las entradas de la tabla [del registro](registry-table.md) y la [tabla RemoveRegistry](removeregistry-table.md), con-1 en la columna raíz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Contexto de instalación](installation-context.md)
</dt> <dt>

[Creación de un solo paquete](single-package-authoring.md)
</dt> </dl>

 

 




