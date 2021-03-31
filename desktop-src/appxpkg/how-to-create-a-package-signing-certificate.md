---
title: How to create an app package signing certificate (Cómo crear un certificado de firma del paquete de la aplicación)
description: Obtenga información sobre cómo usar MakeCert.exe y Pvk2Pfx.exe para crear un certificado de firma de código de prueba, de modo que pueda firmar los paquetes de aplicación de Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077576"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="25e74-103">How to create an app package signing certificate (Cómo crear un certificado de firma del paquete de la aplicación)</span><span class="sxs-lookup"><span data-stu-id="25e74-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25e74-104">MakeCert.exe está en desuso.</span><span class="sxs-lookup"><span data-stu-id="25e74-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="25e74-105">Para obtener instrucciones actuales sobre cómo crear un certificado, consulte [crear un certificado para la firma de paquetes](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="25e74-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="25e74-106">Obtenga información sobre cómo usar [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) para crear un certificado de firma de código de prueba, de modo que pueda firmar los paquetes de aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="25e74-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="25e74-107">Debe firmar digitalmente las aplicaciones de Windows empaquetadas antes de implementarlas.</span><span class="sxs-lookup"><span data-stu-id="25e74-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="25e74-108">Si no usa Microsoft Visual Studio 2012 para crear y firmar los paquetes de la aplicación, debe crear y administrar sus propios certificados de firma de código.</span><span class="sxs-lookup"><span data-stu-id="25e74-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="25e74-109">Puede crear certificados con [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) de Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="25e74-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="25e74-110">Después, puede usar los certificados para firmar los paquetes de la aplicación, de modo que se puedan implementar localmente para realizar pruebas.</span><span class="sxs-lookup"><span data-stu-id="25e74-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="25e74-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="25e74-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="25e74-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="25e74-112">Technologies</span></span>

-   <span data-ttu-id="25e74-113">[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25e74-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="25e74-114">[Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="25e74-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="25e74-115">Herramientas para firmar controladores</span><span class="sxs-lookup"><span data-stu-id="25e74-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="25e74-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25e74-116">Prerequisites</span></span>

-   <span data-ttu-id="25e74-117">Herramientas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) de WDK</span><span class="sxs-lookup"><span data-stu-id="25e74-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="25e74-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="25e74-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="25e74-119">Paso 1: determinar el nombre del publicador del paquete</span><span class="sxs-lookup"><span data-stu-id="25e74-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="25e74-120">Para que el certificado de firma que cree se pueda usar con el paquete de la aplicación que desea firmar, el nombre de sujeto del certificado de firma debe coincidir con el atributo **Publisher** del elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) en el AppxManifest.xml de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="25e74-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="25e74-121">Por ejemplo, supongamos que el AppxManifest.xml contiene:</span><span class="sxs-lookup"><span data-stu-id="25e74-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="25e74-122">Para el parámetro *publisherName* que se especifica con la utilidad [**Makecert**](/windows-hardware/drivers/devtest/makecert) en el paso siguiente, use "CN = contoso software, O = contoso Corporation, C = US".</span><span class="sxs-lookup"><span data-stu-id="25e74-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="25e74-123">Esta cadena de parámetro se especifica entre comillas y distingue entre mayúsculas y minúsculas y el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="25e74-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="25e74-124">La cadena de atributo de **publicador** que se define para el elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) en el AppxManifest.xml debe ser idéntica a la cadena que se especifica con el parámetro [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n para el nombre de sujeto del certificado.</span><span class="sxs-lookup"><span data-stu-id="25e74-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="25e74-125">Copie y pegue la cadena siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="25e74-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="25e74-126">Paso 2: creación de una clave privada con MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="25e74-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="25e74-127">Use la utilidad [**Makecert**](/windows-hardware/drivers/devtest/makecert) para crear un certificado de prueba autofirmado y una clave privada:</span><span class="sxs-lookup"><span data-stu-id="25e74-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="25e74-128">Este comando le pide que proporcione una contraseña para el archivo. PVK.</span><span class="sxs-lookup"><span data-stu-id="25e74-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="25e74-129">Le recomendamos que elija una [contraseña segura](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) y que mantenga la clave privada en una ubicación segura.</span><span class="sxs-lookup"><span data-stu-id="25e74-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="25e74-130">Se recomienda usar los parámetros sugeridos en el ejemplo anterior por estos motivos:</span><span class="sxs-lookup"><span data-stu-id="25e74-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="25e74-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="25e74-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="25e74-132">Crea un certificado raíz autofirmado.</span><span class="sxs-lookup"><span data-stu-id="25e74-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="25e74-133">Esto simplifica la administración del certificado de prueba.</span><span class="sxs-lookup"><span data-stu-id="25e74-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="25e74-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="25e74-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="25e74-135">Marca la restricción básica para el certificado como entidad final.</span><span class="sxs-lookup"><span data-stu-id="25e74-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="25e74-136">Esto impide que el certificado se use como una entidad de certificación (CA) que pueda emitir otros certificados.</span><span class="sxs-lookup"><span data-stu-id="25e74-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="25e74-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="25e74-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="25e74-138">Establece los valores de uso mejorado de clave (EKU) del certificado.</span><span class="sxs-lookup"><span data-stu-id="25e74-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="25e74-139">No incluya un espacio entre los dos valores delimitados por comas.</span><span class="sxs-lookup"><span data-stu-id="25e74-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="25e74-140">1.3.6.1.5.5.7.3.3 indica que el certificado es válido para la firma de código.</span><span class="sxs-lookup"><span data-stu-id="25e74-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="25e74-141">Especifique siempre este valor para limitar el uso previsto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="25e74-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="25e74-142">1.3.6.1.4.1.311.10.3.13 indica que el certificado respeta la firma de la duración.</span><span class="sxs-lookup"><span data-stu-id="25e74-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="25e74-143">Normalmente, si una firma tiene una marca de tiempo, siempre que el certificado sea válido en el momento en que se realizó la marca de tiempo, la firma sigue siendo válida incluso si el certificado expira.</span><span class="sxs-lookup"><span data-stu-id="25e74-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="25e74-144">Este EKU fuerza la expiración de la firma independientemente de si la firma tiene una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="25e74-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="25e74-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="25e74-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="25e74-146">Establece la fecha de expiración del certificado.</span><span class="sxs-lookup"><span data-stu-id="25e74-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="25e74-147">Proporcione un valor para el parámetro *expirationDate* en formato mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="25e74-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="25e74-148">Se recomienda elegir una fecha de expiración solo cuando sea necesario para los fines de prueba, normalmente menos de un año.</span><span class="sxs-lookup"><span data-stu-id="25e74-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="25e74-149">Esta fecha de expiración junto con el EKU de firma de duración puede ayudar a limitar la ventana en la que el certificado puede estar en peligro y usarse inutilizadamente.</span><span class="sxs-lookup"><span data-stu-id="25e74-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="25e74-150">Para obtener más información sobre otras opciones, vea [**Makecert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="25e74-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="25e74-151">Paso 3: crear un archivo de intercambio de información personal (. pfx) mediante Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="25e74-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="25e74-152">Use la utilidad [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para convertir los archivos. PVK y. cer que [**Makecert**](/windows-hardware/drivers/devtest/makecert) creó en un archivo. pfx que puede usar con [SignTool](/windows/desktop/SecCrypto/signtool) para firmar un paquete de aplicación:</span><span class="sxs-lookup"><span data-stu-id="25e74-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="25e74-153">Los archivos *myKey. PVK* y *myKey. cer* son los mismos archivos que [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) creados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="25e74-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="25e74-154">Mediante el parámetro opcional/Po, puede especificar una contraseña diferente para el archivo. pfx resultante. de lo contrario, el archivo. pfx tiene la misma contraseña que *myKey. PVK*.</span><span class="sxs-lookup"><span data-stu-id="25e74-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="25e74-155">Para obtener más información sobre otras opciones, vea [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="25e74-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="25e74-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25e74-156">Remarks</span></span>

<span data-ttu-id="25e74-157">Después de crear el archivo. pfx, puede usar el archivo con [SignTool](/windows/desktop/SecCrypto/signtool) para firmar un paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="25e74-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="25e74-158">Para obtener más información, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="25e74-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="25e74-159">Pero el certificado sigue sin ser de confianza para el equipo local para la implementación de paquetes de aplicaciones hasta que se instala en el almacén de certificados de confianza del equipo local.</span><span class="sxs-lookup"><span data-stu-id="25e74-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="25e74-160">Puede usar [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), que viene con Windows.</span><span class="sxs-lookup"><span data-stu-id="25e74-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="25e74-161">**Para instalar certificados con WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="25e74-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="25e74-162">Ejecute **Cmd.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="25e74-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="25e74-163">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="25e74-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="25e74-164">Se recomienda quitar los certificados si ya no están en uso.</span><span class="sxs-lookup"><span data-stu-id="25e74-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="25e74-165">Desde el mismo símbolo del sistema de administrador, ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="25e74-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="25e74-166">**CertID** es el número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="25e74-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="25e74-167">Ejecute este comando para determinar el número de serie del certificado:</span><span class="sxs-lookup"><span data-stu-id="25e74-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="25e74-168">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="25e74-168">Security Considerations</span></span>

<span data-ttu-id="25e74-169">Al agregar un certificado a los [almacenes de certificados del equipo local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), afecta a la confianza del certificado de todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="25e74-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="25e74-170">Se recomienda instalar los certificados de firma de código que desee para probar paquetes de aplicaciones en el almacén de certificados de personas de confianza.</span><span class="sxs-lookup"><span data-stu-id="25e74-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="25e74-171">Quite los certificados inmediatamente cuando ya no sean necesarios, para evitar que se usen para poner en peligro la confianza del sistema.</span><span class="sxs-lookup"><span data-stu-id="25e74-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25e74-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25e74-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25e74-173">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="25e74-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="25e74-174">Ejemplo de creación de paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="25e74-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="25e74-175">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="25e74-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="25e74-176">[Procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25e74-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="25e74-177">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)</span><span class="sxs-lookup"><span data-stu-id="25e74-177">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
</dt> <dt>

<span data-ttu-id="25e74-178">[Firma de un paquete de la aplicación](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="25e74-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 