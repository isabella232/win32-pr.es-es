---
description: Una lista de las propiedades Windows Installer que dan valores escritos en la clave del Registro Desinstalar.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Propiedades del instalador de la clave del Registro de desinstalación
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171621"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Propiedades del instalador de la clave del Registro de desinstalación

Las siguientes propiedades del instalador dan los valores escritos en la clave del Registro:

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Desinstalación de** \\ **CurrentVersion**

Los valores se almacenan en una subclave identificada por el GUID del código de producto de la aplicación.



| Value               | Windows Propiedad installer                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName,**](productname.md) propiedad                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivado de la [**propiedad ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publisher           | [**Propiedad Fabricante**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivado de la [**propiedad ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivado de la [**propiedad ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versión             | Derivado de la [**propiedad ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**Propiedad ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | [**Propiedad ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | La última vez que este producto recibió el servicio. El valor de esta propiedad se reemplaza cada vez que se aplica o quita una revisión del producto o se usa la opción de línea de comandos [/v](command-line-options.md) para reparar el producto. Si el producto no ha recibido ninguna reparación o revisión, esta propiedad contiene la hora a la que se instaló este producto en este equipo. |
| InstallLocation     | [**Propiedad ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir,**](sourcedir.md) propiedad                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | [**Propiedad ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | [**Propiedad ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**Propiedad ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Comentarios            | [**Propiedad ARPCOMMENTS**](arpcomments.md) <br/> Comentarios proporcionados en el panel de control **Agregar o** quitar programas.<br/>                                                                                                                                                                                                                                |
| Contacto             | [**Propiedad ARPCONTACT**](arpcontact.md) <br/> Póngase en contacto con el panel de control **Agregar o quitar** programas.<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinado y establecido por el Windows programa de instalación.                                                                                                                                                                                                                                                                                                                         |
| Lenguaje            | [**ProductLanguage, propiedad**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinado y establecido por el Windows programa de instalación.                                                                                                                                                                                                                                                                                                                         |
| Léame              | [**Propiedad ARPREADME**](arpreadme.md) <br/> Léame proporcionado en **el panel de** control Agregar o quitar programas.<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinado y establecido por Windows Instalador.                                                                                                                                                                                                                                                                                                                             |
| ConfiguraciónIdentifier  | [**Propiedad MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Configuración de agregar o quitar programas con Windows instalador](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> </dl>

 

 




