---
description: Cómo obtener acceso a las variables de firmware de Unified Extensible Firmware Interface (UEFI) desde una aplicación universal de Windows.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Acceder a las variables de firmware UEFI desde una aplicación universal de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667596"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="57286-103">Acceder a las variables de firmware UEFI desde una aplicación universal de Windows</span><span class="sxs-lookup"><span data-stu-id="57286-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="57286-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="57286-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="57286-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="57286-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="57286-106">Cómo obtener acceso a las variables de firmware de Unified Extensible Firmware Interface (UEFI) desde una aplicación universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="57286-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="57286-107">A partir de Windows 10, versión 1803, las aplicaciones universales de Windows pueden usar [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) y [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (y sus variantes "ex") para tener acceso a las variables de firmware UEFI haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57286-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="57286-108">Declare la funcionalidad personalizada **Microsoft. firmwareRead \_ cw5n1h2txyewy** en el manifiesto para leer una variable de firmware o la capacidad **Microsoft. firmwareWrite \_ cw5n1h2txyewy** para escribir una variable de firmware.</span><span class="sxs-lookup"><span data-stu-id="57286-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="57286-109">Declare también la funcionalidad restringida de **protectedApp** en el manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="57286-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="57286-110">Por ejemplo, las siguientes adiciones de manifiesto de aplicación permiten que la aplicación universal de Windows Lea las variables de firmware:</span><span class="sxs-lookup"><span data-stu-id="57286-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="57286-111">Establezca la opción del vinculador **/INTEGRITYCHECK**, para todas las configuraciones de proyecto, antes de enviar la aplicación a la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="57286-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="57286-112">Esto garantiza que la aplicación se iniciará como una aplicación protegida.</span><span class="sxs-lookup"><span data-stu-id="57286-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="57286-113">Consulte [/INTEGRITYCHECK (requerir comprobación de firma)](/cpp/build/reference/integritycheck-require-signature-check) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="57286-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="57286-114">Obtenga un archivo de [descriptor de funcionalidad personalizado](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) firmado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57286-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="57286-115">Vea [crear una funcionalidad personalizada para emparejar un controlador con una aplicación de soporte de hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) y [usar una funcionalidad personalizada para emparejar una aplicación de soporte de hardware (HSA) con un controlador](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) para obtener información sobre cómo obtener un archivo SCCD firmado de Microsoft, cómo empaquetarlo con su aplicación y cómo habilitar el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="57286-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="57286-116">Este es un archivo SSCD de ejemplo del [ejemplo CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span><span class="sxs-lookup"><span data-stu-id="57286-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="57286-117">Envíe la aplicación a la Microsoft Store para firmarla.</span><span class="sxs-lookup"><span data-stu-id="57286-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="57286-118">Para fines de desarrollo, puede omitir la firma si habilita la firma de prueba en la base de datos de configuración de arranque (BCD).</span><span class="sxs-lookup"><span data-stu-id="57286-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="57286-119">Consulte [la opción de configuración de arranque TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="57286-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57286-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57286-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57286-121">Funcionalidades especiales y restringidas</span><span class="sxs-lookup"><span data-stu-id="57286-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="57286-122">**GetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="57286-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="57286-123">**GetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="57286-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="57286-124">**SetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="57286-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="57286-125">**SetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="57286-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="57286-126">Acceder a la información de SMBIOS desde una aplicación universal de Windows</span><span class="sxs-lookup"><span data-stu-id="57286-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
