---
description: Acceso a la información del BIOS de administración del sistema (SMBIOS) desde una aplicación Windows universal.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Acceso a información de SMBIOS desde una aplicación de Windows universal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764959"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Acceso a información de SMBIOS desde una aplicación de Windows universal

> [NOTA] Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.

Acceso a la información del BIOS de administración del sistema (SMBIOS) desde una aplicación Windows universal.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Acceso a la información de SMBIOS desde una aplicación Windows plataforma universal

A partir de Windows 10, versión 1803, las aplicaciones universales de Windows pueden usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) y [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acceder a la información de SMBIOS declarando la funcionalidad restringida **de smbios** en el manifiesto de aplicación.

> [!IMPORTANT]
> Solo se admite el acceso a tablas de firmware SMBIOS (RSMB) sin procesar desde una aplicación Windows universal. **ACCESO \_ DENIED** se devolverá si intenta acceder a otros tipos de tabla de firmware desde una aplicación de Windows universal.

 

Para declarar la **funcionalidad restringida de smbios** en el manifiesto de aplicación, agregue el espacio de nombres **rescap** y la funcionalidad **smbios** como se muestra a continuación:

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

[Acceso a variables de firmware UEFI desde una aplicación Windows universal](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
