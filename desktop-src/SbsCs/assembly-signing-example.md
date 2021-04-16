---
description: En el ejemplo siguiente se describe cómo generar un ensamblado en paralelo firmado que consta del manifiesto del ensamblado, el catálogo de comprobación y los archivos de ensamblado.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Ejemplo de firma de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105649367"
---
# <a name="assembly-signing-example"></a><span data-ttu-id="a1fd1-103">Ejemplo de firma de ensamblado</span><span class="sxs-lookup"><span data-stu-id="a1fd1-103">Assembly Signing Example</span></span>

<span data-ttu-id="a1fd1-104">En el ejemplo siguiente se describe cómo generar un ensamblado en paralelo firmado que consta del manifiesto del ensamblado, el catálogo de comprobación y los archivos de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="a1fd1-105">Los ensamblados en paralelo compartidos deben estar firmados.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="a1fd1-106">El sistema operativo comprueba la firma del ensamblado antes de instalar un ensamblado compartido en la tienda en paralelo global (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="a1fd1-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="a1fd1-107">Esto dificulta la suplantación del publicador del ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="a1fd1-108">Tenga en cuenta que al cambiar los archivos de ensamblado o el contenido del manifiesto después de generar el catálogo de ensamblados, se invalida el catálogo y el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="a1fd1-109">Si debe actualizar los archivos de ensamblado o el manifiesto después de crear y firmar el catálogo, debe firmar de nuevo el ensamblado y generar un nuevo catálogo.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="a1fd1-110">Comience con los archivos de ensamblado, el manifiesto del ensamblado y el archivo de certificado que utilizará para firmar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="a1fd1-111">El archivo de certificado debe tener un tamaño de 2048 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="a1fd1-112">No es necesario usar un certificado de confianza.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="a1fd1-113">El certificado solo se usa para comprobar que el ensamblado no se ha dañado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="a1fd1-114">Ejecute la utilidad [Pktextract.exe](pktextract-exe.md) proporcionada en el kit de desarrollo de software (SDK) de Microsoft Windows para extraer el token de clave pública del archivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="a1fd1-115">Para que Pktextract funcione correctamente, el archivo de certificado debe estar presente en el mismo directorio que la utilidad.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="a1fd1-116">Use el valor del token de clave pública extraído para actualizar el atributo **PublicKeyToken** del elemento **assemblyIdentity** en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="a1fd1-117">Este es un ejemplo de un archivo de manifiesto denominado MySampleAssembly. manifest.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="a1fd1-118">El ensamblado MySampleAssembly contiene un solo archivo, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="a1fd1-119">Tenga en cuenta que el valor del atributo **PublicKeyToken** del elemento **assemblyIdentity** se ha actualizado con el valor del token de clave pública.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

<span data-ttu-id="a1fd1-120">A continuación, ejecute la utilidad [Mt.exe](mt-exe.md) proporcionada en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="a1fd1-121">Los archivos de ensamblado deben encontrarse en el mismo directorio que el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="a1fd1-122">En este ejemplo, este es el directorio MySampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="a1fd1-123">Llame a Mt.exe para el ejemplo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a1fd1-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="a1fd1-124">**c: \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="a1fd1-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="a1fd1-125">Este es el aspecto del manifiesto de ejemplo después de ejecutar Mt.exe.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="a1fd1-126">Observe que la ejecución de Mt.exe con la opción hashupdate agrega el hash SHA-1 del archivo.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="a1fd1-127">No cambie este valor.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-127">Do not change this value.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

<span data-ttu-id="a1fd1-128">La ejecución de Mt.exe con la opción-makecdfs genera un archivo denominado MySampleAssembly. manifest. CDF que describe el contenido del catálogo de seguridad que se usará para validar el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="a1fd1-129">El siguiente paso consiste en ejecutar Makecat.exe sobre este. CDF para crear el catálogo de seguridad para el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="a1fd1-130">La llamada a Makecat.exe para este ejemplo aparecería de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a1fd1-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="a1fd1-131">**c: \\ MySampleAssembly>Makecat MySampleAssembly. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="a1fd1-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="a1fd1-132">El paso final consiste en ejecutar SignTool.exe para firmar el archivo de catálogo con el certificado.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="a1fd1-133">Debe ser el mismo certificado que se usó en el anterior para generar el token de clave pública.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="a1fd1-134">Para obtener más información sobre SignTool.exe consulte el tema de [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="a1fd1-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="a1fd1-135">La llamada a **SignTool** para el ejemplo aparecería de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a1fd1-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="a1fd1-136">**c: \\ MySampleAssembly>SignTool Sign/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="a1fd1-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="a1fd1-137">Si tiene un certificado digital autenticado y la entidad de certificación usa el formato de archivo PVK para almacenar la clave privada, puede usar el importador de archivos de certificado digital de PVK (pvkimprt.exe) para importar la clave en el proveedor de servicios criptográficos (CSP).</span><span class="sxs-lookup"><span data-stu-id="a1fd1-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="a1fd1-138">Esta utilidad permite exportar al formato estándar del sector de PFX/P12.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="a1fd1-139">Para obtener más información sobre el importador de archivos de certificado digital de PVK, vea la sección recursos de implementación de MSDN Library o póngase en contacto con la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="a1fd1-140">Es posible que pueda obtener pvkimprt.exe de https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="a1fd1-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="a1fd1-141">Vea también [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="a1fd1-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
