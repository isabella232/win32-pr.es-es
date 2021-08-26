---
description: Una lista de las propiedades Windows Installer que dan valores escritos en la clave del Registro Desinstalar.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Propiedades del instalador de la clave del Registro de desinstalación
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810325"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Propiedades del instalador de la clave del Registro de desinstalación

Las siguientes propiedades del instalador dan los valores escritos en la clave del Registro:

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Desinstalación de** \\ **CurrentVersion**

Los valores se almacenan en una subclave identificada por el GUID del código de producto de la aplicación.



| Valor               | Windows Propiedad installer                                                                                                                                                                                                                                                                                                                                           |
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
| EstimatedSize       | Determinado y establecido por el Windows instalador.                                                                                                                                                                                                                                                                                                                         |
| Lenguaje            | [**ProductLanguage, propiedad**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinado y establecido por el Windows instalador.                                                                                                                                                                                                                                                                                                                         |
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

 

 




