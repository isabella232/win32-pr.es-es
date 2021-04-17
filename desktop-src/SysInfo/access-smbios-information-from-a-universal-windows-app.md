---
description: Cómo obtener acceso a la información del BIOS de administración del sistema (SMBIOS) desde una aplicación universal de Windows.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Acceder a la información de SMBIOS desde una aplicación universal de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545782"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Acceder a la información de SMBIOS desde una aplicación universal de Windows

> Tenga en cuenta Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.

Cómo obtener acceso a la información del BIOS de administración del sistema (SMBIOS) desde una aplicación universal de Windows.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Acceder a la información de SMBIOS desde una aplicación Plataforma universal de Windows

A partir de Windows 10, versión 1803, las aplicaciones universales de Windows pueden usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) y [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acceder a la información de SMBIOS mediante la declaración de la capacidad restringida de **SMBIOS** en el manifiesto de la aplicación.

> [!IMPORTANT]
> Solo se admite el acceso a tablas de firmware de SMBIOS sin procesar (RSMB) desde una aplicación universal de Windows. **Acceso a \_ Denegado** se devolverá si intenta tener acceso a otros tipos de tabla de firmware desde una aplicación universal de Windows.

 

Para declarar la funcionalidad restringida de **SMBIOS** en el manifiesto de la aplicación, agregue el espacio de nombres **ResCap** y la capacidad de **SMBIOS** como se indica a continuación:

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funcionalidades especiales y restringidas](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[Acceder a las variables de firmware UEFI desde una aplicación universal de Windows](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
