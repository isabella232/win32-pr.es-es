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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Acceder a las variables de firmware UEFI desde una aplicación universal de Windows

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Cómo obtener acceso a las variables de firmware de Unified Extensible Firmware Interface (UEFI) desde una aplicación universal de Windows.

A partir de Windows 10, versión 1803, las aplicaciones universales de Windows pueden usar [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) y [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (y sus variantes "ex") para tener acceso a las variables de firmware UEFI haciendo lo siguiente:

-   Declare la funcionalidad personalizada **Microsoft. firmwareRead \_ cw5n1h2txyewy** en el manifiesto para leer una variable de firmware o la capacidad **Microsoft. firmwareWrite \_ cw5n1h2txyewy** para escribir una variable de firmware.
-   Declare también la funcionalidad restringida de **protectedApp** en el manifiesto de la aplicación.
-   Por ejemplo, las siguientes adiciones de manifiesto de aplicación permiten que la aplicación universal de Windows Lea las variables de firmware:

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

-   Establezca la opción del vinculador **/INTEGRITYCHECK**, para todas las configuraciones de proyecto, antes de enviar la aplicación a la Microsoft Store. Esto garantiza que la aplicación se iniciará como una aplicación protegida. Consulte [/INTEGRITYCHECK (requerir comprobación de firma)](/cpp/build/reference/integritycheck-require-signature-check) para obtener más información.
-   Obtenga un archivo de [descriptor de funcionalidad personalizado](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) firmado de Microsoft. Vea [crear una funcionalidad personalizada para emparejar un controlador con una aplicación de soporte de hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) y [usar una funcionalidad personalizada para emparejar una aplicación de soporte de hardware (HSA) con un controlador](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) para obtener información sobre cómo obtener un archivo SCCD firmado de Microsoft, cómo empaquetarlo con su aplicación y cómo habilitar el modo de desarrollador. Este es un archivo SSCD de ejemplo del [ejemplo CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):
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

    

-   Envíe la aplicación a la Microsoft Store para firmarla. Para fines de desarrollo, puede omitir la firma si habilita la firma de prueba en la base de datos de configuración de arranque (BCD). Consulte [la opción de configuración de arranque TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funcionalidades especiales y restringidas](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**GetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**SetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Acceder a la información de SMBIOS desde una aplicación universal de Windows](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
