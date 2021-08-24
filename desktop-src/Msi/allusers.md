---
Description: La propiedad ALLUSERS configura el contexto de instalación del paquete.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS, propiedad
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: b6412707d6ef46b55d1f8add3de56a24e6f970dc9fa7f0353dce6ec9efa9f531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581885"
---
# <a name="allusers-property"></a>ALLUSERS, propiedad

La **propiedad ALLUSERS** configura el contexto de instalación del paquete. El instalador de Windows realiza una instalación por usuario o por máquina en función de los privilegios de acceso del usuario, si se requieren privilegios elevados para instalar la aplicación, el valor de la propiedad **ALLUSERS,** el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) y la versión del sistema operativo.

El valor de la **propiedad ALLUSERS,** en el momento de la instalación, determina el contexto [de instalación](installation-context.md).

-   Un **valor de propiedad ALLUSERS** de 1 especifica el contexto de instalación por equipo.
-   Un **valor de propiedad ALLUSERS** de una cadena vacía ("") especifica el contexto de instalación por usuario.
-   Si el valor de la propiedad **ALLUSERS** se establece en 2, el instalador de Windows siempre restablece el valor de la propiedad **ALLUSERS** en 1 y realiza una instalación por equipo o restablece el valor de la propiedad **ALLUSERS** en una cadena vacía ("") y realiza una instalación por usuario. El valor ALLUSERS=2 permite al sistema restablecer el valor de **ALLUSERS** y el contexto de instalación, en función de los privilegios del usuario y la versión de Windows.

    **Windows 7:** Establezca la **propiedad ALLUSERS** en 2 para usar la [**propiedad MSIINSTALLPERUSER**](msiinstallperuser.md) para especificar el contexto de instalación. Establezca la **propiedad MSIINSTALLPERUSER** en una cadena vacía ("") para una instalación por equipo. Establezca la **propiedad MSIINSTALLPERUSER** en 1 para una instalación por usuario. Si el paquete se ha escrito siguiendo las directrices de desarrollo descritas en Creación de paquete [único,](single-package-authoring.md)los usuarios con acceso de usuario pueden instalarse en el contexto por usuario sin tener que proporcionar credenciales de UAC. Si el usuario tiene privilegios de acceso de usuario, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo UAC.

    **Windows Vista:** Establezca la **propiedad ALLUSERS** en 2 y Windows Installer cumple con el [*Control de cuentas de usuario*](u-gly.md) (UAC). Si el usuario tiene privilegios de acceso de usuario y ALLUSERS=2, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo UAC. Si UAC está habilitado y no se proporcionan las credenciales de administrador correctas, se produce un error en la instalación que indica que se requieren privilegios de administrador. Si UAC está deshabilitado por la clave del Registro, la directiva de grupo o el panel de control, no se muestra el cuadro de diálogo UAC y se produce un error en la instalación que indica que se requieren privilegios de administrador.

    **Windows XP:** Establezca la **propiedad ALLUSERS** en 2 y Windows Installer realiza una instalación por usuario si el usuario tiene privilegios de acceso de usuario.

-   Si el valor de la **propiedad ALLUSERS** no es igual a 2, Windows Installer omite el valor de la [**propiedad MSIINSTALLPERUSER.**](msiinstallperuser.md)

## <a name="example"></a>Ejemplo

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) en GitHub.

## <a name="default-value"></a>Valor predeterminado

El contexto de instalación predeterminado recomendado es por usuario. Si **ALLUSERS** no está establecido, el instalador realiza una instalación por usuario. Puede asegurarse de que no se ha establecido la propiedad **ALLUSERS** estableciendo su valor en una cadena vacía (""), ALLUSERS="".

## <a name="remarks"></a>Comentarios

El [](installation-context.md) contexto de instalación determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder.**](commonfiles64folder.md) El contexto de instalación determina las partes del registro donde se escriben o quitan las entradas de la tabla [Registry](registry-table.md) y [removeRegistry](removeregistry-table.md), con -1 en la columna Raíz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Contexto de instalación](installation-context.md)
</dt> <dt>

[Creación de paquetes únicos](single-package-authoring.md)
</dt> </dl>

 

 




