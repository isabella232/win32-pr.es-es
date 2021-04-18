---
description: Una lista de las propiedades de Windows Installer que proporcionan valores escritos en la clave del registro Uninstall.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Installer propiedades de la clave del registro Uninstall
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994503"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Installer propiedades de la clave del registro Uninstall

Las siguientes propiedades del instalador proporcionan los valores escritos en la clave del registro:

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

Los valores se almacenan en una subclave identificada por el GUID del código de producto de la aplicación.



| Value               | Propiedad Windows Installer                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName**](productname.md) (propiedad)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivado de la propiedad [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publicador           | Propiedad [**manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivado de la propiedad [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivado de la propiedad [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versión             | Derivado de la propiedad [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | Propiedad [**ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | Propiedad [**ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | La última vez que este producto recibió el servicio. El valor de esta propiedad se reemplaza cada vez que se aplica o quita una revisión del producto o se usa la [opción de línea de comandos](command-line-options.md) /v para reparar el producto. Si el producto no ha recibido ninguna reparación o revisión, esta propiedad contiene la hora en que se instaló este producto en este equipo. |
| InstallLocation     | Propiedad [**ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | Propiedad [**SourceDir**](sourcedir.md)                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | Propiedad [**ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | Propiedad [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | Propiedad [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Comentarios            | Propiedad [**ARPCOMMENTS**](arpcomments.md) <br/> Comentarios proporcionados en el panel de control **Agregar o quitar programas** .<br/>                                                                                                                                                                                                                                |
| Contacto             | Propiedad [**ARPCONTACT**](arpcontact.md) <br/> Contacto proporcionado al panel de control **Agregar o quitar programas** .<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinados y establecidos por el Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Idioma            | Propiedad [**ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinados y establecidos por el Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Léame              | Propiedad [**ARPREADME**](arpreadme.md) <br/> Archivo Léame proporcionado en el panel de control **Agregar o quitar programas** .<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinado y establecido por Windows Installer.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | Propiedad [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Configuración de agregar o quitar programas con Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> </dl>

 

 




