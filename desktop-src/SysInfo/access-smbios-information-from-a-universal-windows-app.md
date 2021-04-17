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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="3da2e-103">Acceder a la información de SMBIOS desde una aplicación universal de Windows</span><span class="sxs-lookup"><span data-stu-id="3da2e-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="3da2e-104">Tenga en cuenta Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3da2e-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3da2e-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.</span><span class="sxs-lookup"><span data-stu-id="3da2e-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="3da2e-106">Cómo obtener acceso a la información del BIOS de administración del sistema (SMBIOS) desde una aplicación universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="3da2e-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="3da2e-107">Acceder a la información de SMBIOS desde una aplicación Plataforma universal de Windows</span><span class="sxs-lookup"><span data-stu-id="3da2e-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="3da2e-108">A partir de Windows 10, versión 1803, las aplicaciones universales de Windows pueden usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) y [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acceder a la información de SMBIOS mediante la declaración de la capacidad restringida de **SMBIOS** en el manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3da2e-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3da2e-109">Solo se admite el acceso a tablas de firmware de SMBIOS sin procesar (RSMB) desde una aplicación universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="3da2e-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="3da2e-110">**Acceso a \_ Denegado** se devolverá si intenta tener acceso a otros tipos de tabla de firmware desde una aplicación universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="3da2e-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="3da2e-111">Para declarar la funcionalidad restringida de **SMBIOS** en el manifiesto de la aplicación, agregue el espacio de nombres **ResCap** y la capacidad de **SMBIOS** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="3da2e-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3da2e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3da2e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3da2e-113">Funcionalidades especiales y restringidas</span><span class="sxs-lookup"><span data-stu-id="3da2e-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="3da2e-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="3da2e-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="3da2e-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="3da2e-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="3da2e-116">Acceder a las variables de firmware UEFI desde una aplicación universal de Windows</span><span class="sxs-lookup"><span data-stu-id="3da2e-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
