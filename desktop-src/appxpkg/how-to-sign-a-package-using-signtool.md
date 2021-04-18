---
title: Cómo firmar un paquete de la aplicación con SignTool
description: Obtenga información sobre cómo usar SignTool para firmar los paquetes de aplicación de Windows para que se puedan implementar.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105705059"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="94897-103">Cómo firmar un paquete de la aplicación con SignTool</span><span class="sxs-lookup"><span data-stu-id="94897-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="94897-104">Para firmar un paquete de aplicación de Windows, consulte [firmar un paquete de aplicación mediante SignTool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="94897-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="94897-105">Obtenga información sobre cómo usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar los paquetes de aplicación de Windows para que se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="94897-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="94897-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) forma parte del kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="94897-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="94897-107">Todos los paquetes de aplicaciones de Windows deben firmarse digitalmente para poder implementarlos.</span><span class="sxs-lookup"><span data-stu-id="94897-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="94897-108">Aunque Microsoft Visual Studio 2012 y versiones posteriores pueden firmar un paquete de aplicación durante su creación, los paquetes que se crean con la herramienta de [Empaquetador de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) del Windows SDK no se firman.</span><span class="sxs-lookup"><span data-stu-id="94897-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="94897-109">Solo puede usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar los paquetes de aplicación de Windows en Windows 8 y versiones posteriores, o en windows Server 2012 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="94897-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="94897-110">No se puede usar **SignTool** para firmar paquetes de aplicación en sistemas operativos de nivel inferior, como Windows 7 o windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="94897-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="94897-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="94897-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="94897-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="94897-112">Technologies</span></span>

-   <span data-ttu-id="94897-113">[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94897-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="94897-114">[Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="94897-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="94897-115">Herramientas para firmar archivos y comprobar firmas</span><span class="sxs-lookup"><span data-stu-id="94897-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="94897-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="94897-116">Prerequisites</span></span>

-   <span data-ttu-id="94897-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), que forma parte de la Windows SDK</span><span class="sxs-lookup"><span data-stu-id="94897-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="94897-118">Un certificado de firma de código válido, por ejemplo, un archivo de intercambio de información personal (. pfx) creado con las herramientas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)</span><span class="sxs-lookup"><span data-stu-id="94897-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="94897-119">Para obtener información sobre cómo crear un certificado de firma de código válido, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="94897-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="94897-120">Una aplicación empaquetada de Windows, por ejemplo, un archivo. appx creado mediante la herramienta de [Empaquetador de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)</span><span class="sxs-lookup"><span data-stu-id="94897-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="94897-121">**Consideraciones adicionales**</span><span class="sxs-lookup"><span data-stu-id="94897-121">**Additional considerations**</span></span>

<span data-ttu-id="94897-122">El certificado que se usa para firmar el paquete de la aplicación debe cumplir estos criterios:</span><span class="sxs-lookup"><span data-stu-id="94897-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="94897-123">El nombre de sujeto del certificado debe coincidir con el atributo de **publicador** que se encuentra en el elemento de [**identidad**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del archivo de AppxManifest.xml que está almacenado en el paquete.</span><span class="sxs-lookup"><span data-stu-id="94897-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="94897-124">El nombre del publicador forma parte de la identidad de una aplicación de Windows empaquetada, por lo que tiene que hacer que el nombre del firmante del certificado coincida con el nombre del publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="94897-125">Esto permite comprobar la identidad de los paquetes firmados con respecto a la firma digital.</span><span class="sxs-lookup"><span data-stu-id="94897-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="94897-126">Para obtener información sobre los errores de firma que pueden surgir al firmar un paquete de aplicación mediante [**SignTool**](/windows-hardware/drivers/devtest/signtool), consulte la sección Comentarios de [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="94897-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="94897-127">El certificado debe ser válido para la firma de código.</span><span class="sxs-lookup"><span data-stu-id="94897-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="94897-128">Esto significa que ambos elementos deben cumplirse:</span><span class="sxs-lookup"><span data-stu-id="94897-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="94897-129">El campo de uso mejorado de clave (EKU) del certificado debe estar desactivado o contener el valor de EKU para la firma de código (1.3.6.1.5.5.7.3.3).</span><span class="sxs-lookup"><span data-stu-id="94897-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="94897-130">El campo de uso de clave (KU) del certificado debe estar desactivado o contener el bit de uso de la firma digital (0x80).</span><span class="sxs-lookup"><span data-stu-id="94897-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="94897-131">El certificado contiene una clave privada.</span><span class="sxs-lookup"><span data-stu-id="94897-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="94897-132">El certificado es válido.</span><span class="sxs-lookup"><span data-stu-id="94897-132">The certificate is valid.</span></span> <span data-ttu-id="94897-133">Está activo, no ha expirado y no se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="94897-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="94897-134">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="94897-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="94897-135">Paso 1: determinar el algoritmo hash que se va a usar</span><span class="sxs-lookup"><span data-stu-id="94897-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="94897-136">Al firmar el paquete de la aplicación, debe usar el mismo algoritmo hash que utilizó al crear el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="94897-137">Si ha usado los valores predeterminados para crear el paquete de la aplicación, el algoritmo hash usado es SHA256.</span><span class="sxs-lookup"><span data-stu-id="94897-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="94897-138">Si usó el Empaquetador de aplicaciones con un algoritmo hash específico para crear el paquete de la aplicación, use el mismo algoritmo para firmar el paquete.</span><span class="sxs-lookup"><span data-stu-id="94897-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="94897-139">Para determinar el algoritmo hash que se va a utilizar para firmar un paquete, puede extraer el contenido del paquete e inspeccionar el archivo de AppxBlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="94897-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="94897-140">El atributo **HashMethod** del elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica el algoritmo hash que se usó al crear el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="94897-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="94897-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="94897-142">El elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) anterior indica que se ha utilizado el algoritmo SHA256.</span><span class="sxs-lookup"><span data-stu-id="94897-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="94897-143">En esta tabla se muestra la asignación de los algoritmos disponibles actualmente:</span><span class="sxs-lookup"><span data-stu-id="94897-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="94897-144">Valor **HashMethod**</span><span class="sxs-lookup"><span data-stu-id="94897-144">**HashMethod** value</span></span>                            | <span data-ttu-id="94897-145">*hashAlgorithm* que se va a usar</span><span class="sxs-lookup"><span data-stu-id="94897-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="94897-146">SHA256 (valor predeterminado de. appx)</span><span class="sxs-lookup"><span data-stu-id="94897-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="94897-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="94897-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="94897-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="94897-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="94897-149">Paso 2: ejecutar SignTool.exe para firmar el paquete</span><span class="sxs-lookup"><span data-stu-id="94897-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="94897-150">**Para firmar el paquete con un certificado de firma desde un archivo. pfx**</span><span class="sxs-lookup"><span data-stu-id="94897-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="94897-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) toma como valor predeterminado el parámetro/FD *hashAlgorithm* en SHA1 si no se especifica y SHA1 no es válido para firmar paquetes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="94897-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="94897-152">Por lo tanto, debe especificar este parámetro al firmar un paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="94897-153">Para firmar un paquete de aplicación que se creó con el hash SHA256 predeterminado, debe especificar el parámetro/FD *hashAlgorithm* como SHA256:</span><span class="sxs-lookup"><span data-stu-id="94897-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="94897-154">Puede omitir el parámetro/p *password* si usa un archivo. pfx que no está protegido por contraseña.</span><span class="sxs-lookup"><span data-stu-id="94897-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="94897-155">También puede usar otras opciones de selección de certificados compatibles con [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar paquetes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="94897-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="94897-156">Para obtener más información sobre estas opciones, consulte [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="94897-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="94897-157">No se puede usar la operación de marca de tiempo de [**SignTool**](/windows-hardware/drivers/devtest/signtool) en un paquete de aplicación firmado. la operación no es compatible.</span><span class="sxs-lookup"><span data-stu-id="94897-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="94897-158">Si desea realizar una marca de tiempo en el paquete de la aplicación, debe hacerlo durante la operación de firma.</span><span class="sxs-lookup"><span data-stu-id="94897-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="94897-159">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="94897-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="94897-160">Haga que el parámetro/tr *timestampServerUrl* sea igual a la dirección URL de un servidor de marca de tiempo RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="94897-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="94897-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94897-161">Remarks</span></span>

<span data-ttu-id="94897-162">En esta sección se describe la solución de errores de firma para paquetes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="94897-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="94897-163">Solución de problemas de errores de firma de paquetes de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="94897-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="94897-164">Además de los errores de firma que [**SignTool**](/windows-hardware/drivers/devtest/signtool) puede devolver, **SignTool** también puede devolver errores específicos de la firma de paquetes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="94897-165">Estos errores suelen aparecer como errores internos:</span><span class="sxs-lookup"><span data-stu-id="94897-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="94897-166">Si el código de error comienza con 0x8008, como 0x80080206 APPX \_ E \_ daño en \_ el contenido, indica que el paquete que se está firmando no es válido.</span><span class="sxs-lookup"><span data-stu-id="94897-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="94897-167">En este caso, antes de poder firmar el paquete, debe volver a generar el paquete.</span><span class="sxs-lookup"><span data-stu-id="94897-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="94897-168">Para obtener la lista completa de \* errores de 0x8008, consulte [**códigos de error com (seguridad y configuración)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="94897-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="94897-169">Lo más habitual es que el error sea 0x8007000b (ERROR de \_ \_ formato incorrecto).</span><span class="sxs-lookup"><span data-stu-id="94897-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="94897-170">En este caso, puede encontrar información de error más específica en el registro de eventos:</span><span class="sxs-lookup"><span data-stu-id="94897-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="94897-171">**Para buscar en el registro de eventos**</span><span class="sxs-lookup"><span data-stu-id="94897-171">**To search the event log**</span></span>

1.  <span data-ttu-id="94897-172">Ejecute eventvwr. msc.</span><span class="sxs-lookup"><span data-stu-id="94897-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="94897-173">Abra el registro de eventos: Visor de eventos (local) > registros de aplicaciones y servicios > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="94897-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="94897-174">Busque el evento de error más reciente.</span><span class="sxs-lookup"><span data-stu-id="94897-174">Look for the most recent error event.</span></span>

<span data-ttu-id="94897-175">El error interno suele corresponder a uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="94897-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94897-176">Id. de evento</span><span class="sxs-lookup"><span data-stu-id="94897-176">Event ID</span></span></th>
<th><span data-ttu-id="94897-177">Ejemplo de cadena de evento</span><span class="sxs-lookup"><span data-stu-id="94897-177">Example event string</span></span></th>
<th><span data-ttu-id="94897-178">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="94897-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94897-179">150</span><span class="sxs-lookup"><span data-stu-id="94897-179">150</span></span></td>
<td><span data-ttu-id="94897-180">error 0x8007000B: el nombre del publicador del manifiesto de la aplicación (CN = contoso) debe coincidir con el nombre del firmante del certificado de firma (CN = Contoso, C = US).</span><span class="sxs-lookup"><span data-stu-id="94897-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="94897-181">El nombre del publicador del manifiesto de la aplicación debe coincidir exactamente con el nombre de sujeto de la firma.</span><span class="sxs-lookup"><span data-stu-id="94897-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="94897-182">Estos nombres se especifican entre comillas y distinguen mayúsculas de minúsculas y espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="94897-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="94897-183">Puede actualizar la cadena de atributo de <strong>publicador</strong> que se define para el elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> del archivo AppxManifest.xml para que coincida con el nombre de sujeto del certificado de firma previsto.</span><span class="sxs-lookup"><span data-stu-id="94897-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="94897-184">O bien, seleccione otro certificado de firma con un nombre de sujeto que coincida con el nombre del publicador del manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="94897-185">El nombre del publicador del manifiesto y el nombre del firmante del certificado se muestran en el mensaje del evento.</span><span class="sxs-lookup"><span data-stu-id="94897-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94897-186">151</span><span class="sxs-lookup"><span data-stu-id="94897-186">151</span></span></td>
<td><span data-ttu-id="94897-187">error 0x8007000B: el método hash de firma especificado (SHA512) debe coincidir con el método hash usado en la asignación de bloques de paquete de aplicación (SHA256).</span><span class="sxs-lookup"><span data-stu-id="94897-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="94897-188">El hashAlgorithm especificado en el parámetro/FD es incorrecto (vea el paso 1: determinar el algoritmo hash que se debe usar).</span><span class="sxs-lookup"><span data-stu-id="94897-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="94897-189">Vuelva a ejecutar <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> con el hashAlgorithm que coincida con la asignación de bloques del paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94897-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94897-190">152</span><span class="sxs-lookup"><span data-stu-id="94897-190">152</span></span></td>
<td><span data-ttu-id="94897-191">error 0x8007000B: el contenido del paquete de la aplicación debe validarse con su asignación de bloques.</span><span class="sxs-lookup"><span data-stu-id="94897-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="94897-192">El paquete de la aplicación está dañado y debe volver a generarse para generar una nueva asignación de bloques.</span><span class="sxs-lookup"><span data-stu-id="94897-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="94897-193">Para obtener más información sobre cómo crear un paquete de la aplicación, consulta crear un paquete de la aplicación con el <a href="make-appx-package--makeappx-exe-.md">Empaquetador de aplicaciones</a> o <a href="/previous-versions/hh975357(v=vs.110)">crear un paquete de la aplicación con Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="94897-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="94897-194">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="94897-194">Security Considerations</span></span>

<span data-ttu-id="94897-195">Una vez firmado el paquete, el certificado que se usó para firmar el paquete todavía debe ser de confianza para el equipo en el que se va a implementar el paquete.</span><span class="sxs-lookup"><span data-stu-id="94897-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="94897-196">Al agregar un certificado a los [almacenes de certificados del equipo local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), afecta a la confianza del certificado de todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="94897-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="94897-197">Se recomienda que instale los certificados de firma de código que desee para probar paquetes de aplicaciones en el almacén de certificados de personas de confianza y que quite los certificados cuando ya no sea necesario.</span><span class="sxs-lookup"><span data-stu-id="94897-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="94897-198">Si crea sus propios certificados de prueba para firmar paquetes de aplicaciones, también se recomienda restringir los privilegios asociados al certificado de prueba.</span><span class="sxs-lookup"><span data-stu-id="94897-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="94897-199">Para obtener más información sobre cómo crear certificados de prueba para firmar paquetes de aplicaciones, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="94897-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94897-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94897-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="94897-201">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="94897-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="94897-202">Ejemplo de creación de paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="94897-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="94897-203">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="94897-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="94897-204">[Procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94897-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="94897-205">[Firmar un paquete en Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="94897-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="94897-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="94897-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="94897-207">Paquete de aplicaciones (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="94897-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

<span data-ttu-id="94897-208">[How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md) (Cómo crear un certificado de firma del paquete de la aplicación)</span><span class="sxs-lookup"><span data-stu-id="94897-208">[How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md)</span></span>
</dt> </dl>

