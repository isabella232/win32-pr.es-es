---
description: Crea un certificado X. 509, firmado por la clave raíz de prueba u otra clave especificada, que enlaza su nombre a la parte pública del par de claves. El certificado se guarda en un archivo, un almacén de certificados del sistema o ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686873"
---
# <a name="makecert"></a><span data-ttu-id="81c5b-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="81c5b-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="81c5b-105">Makecert está en desuso.</span><span class="sxs-lookup"><span data-stu-id="81c5b-105">MakeCert is deprecated.</span></span> <span data-ttu-id="81c5b-106">Para crear certificados autofirmados, use el cmdlet [de PowerShell New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="81c5b-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="81c5b-107">La herramienta MakeCert crea un certificado [*X. 509*](../secgloss/x-gly.md) , firmado por la clave raíz de prueba u otra clave especificada, que enlaza su nombre a la parte pública del par de claves.</span><span class="sxs-lookup"><span data-stu-id="81c5b-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="81c5b-108">El certificado se guarda en un archivo, un almacén de certificados del sistema o ambos.</span><span class="sxs-lookup"><span data-stu-id="81c5b-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="81c5b-109">La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="81c5b-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="81c5b-110">La herramienta MakeCert usa la siguiente sintaxis de comando:</span><span class="sxs-lookup"><span data-stu-id="81c5b-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="81c5b-111">**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="81c5b-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="81c5b-112">*OutputFile* es el nombre del archivo donde se escribirá el certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="81c5b-113">Puede omitir *OutputFile* si el certificado no se va a escribir en un archivo.</span><span class="sxs-lookup"><span data-stu-id="81c5b-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="81c5b-114">Opciones</span><span class="sxs-lookup"><span data-stu-id="81c5b-114">Options</span></span>

<span data-ttu-id="81c5b-115">MakeCert incluye opciones básicas y extendidas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="81c5b-116">Las opciones básicas son las que más se utilizan para crear un certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="81c5b-117">Las opciones ampliadas proporcionan más flexibilidad.</span><span class="sxs-lookup"><span data-stu-id="81c5b-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="81c5b-118">Las opciones de MakeCert también se dividen en tres grupos funcionales:</span><span class="sxs-lookup"><span data-stu-id="81c5b-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="81c5b-119">Opciones básicas específicas de la tecnología de almacén de certificados únicamente.</span><span class="sxs-lookup"><span data-stu-id="81c5b-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="81c5b-120">Opciones extendidas específicas de la tecnología de clave privada y archivos SPC únicamente.</span><span class="sxs-lookup"><span data-stu-id="81c5b-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="81c5b-121">Opciones extendidas aplicables a la tecnología de archivos SPC, clave privada y almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="81c5b-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="81c5b-122">Las opciones que se proporcionan en las tablas siguientes solo se pueden usar con Internet Explorer 4,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="81c5b-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81c5b-123">Opción básica</span><span class="sxs-lookup"><span data-stu-id="81c5b-123">Basic option</span></span></th>
<th><span data-ttu-id="81c5b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="81c5b-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81c5b-125"><strong>-a</strong> <strong></strong> <em>Algoritmo</em> de</span><span class="sxs-lookup"><span data-stu-id="81c5b-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="81c5b-126">Algoritmo <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> .</span><span class="sxs-lookup"><span data-stu-id="81c5b-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="81c5b-127">Debe establecerse en <strong>SHA-1</strong> o <strong>MD5</strong> (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="81c5b-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="81c5b-128">Para obtener información acerca de MD5, consulte <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="81c5b-130">Fecha en que el certificado pasa a ser válido por primera vez.</span><span class="sxs-lookup"><span data-stu-id="81c5b-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="81c5b-131">El valor predeterminado es cuando se crea el certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-131">The default is when the certificate is created.</span></span> <span data-ttu-id="81c5b-132">El formato de <em>DateStart</em> es mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="81c5b-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-133"><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="81c5b-134">Tipo de certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-134">Certificate type.</span></span> <span data-ttu-id="81c5b-135"><em>CertificateTypes</em> puede ser <strong>End</strong> para la entidad de certificación o <strong>autoridad</strong> para la <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="81c5b-137">Fecha en que finaliza el período de validez.</span><span class="sxs-lookup"><span data-stu-id="81c5b-137">Date when the validity period ends.</span></span> <span data-ttu-id="81c5b-138">El valor predeterminado es el año 2039.</span><span class="sxs-lookup"><span data-stu-id="81c5b-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="81c5b-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="81c5b-140">Inserta en el certificado una lista de uno o varios <a href="/windows/desktop/SecGloss/o-gly"><em>identificadores de objeto</em></a> (OID) de <a href="/windows/desktop/SecGloss/e-gly"><em>uso de clave mejorados</em></a> por comas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="81c5b-141">Por ejemplo, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> inserta el OID de autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="81c5b-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="81c5b-142">Para obtener definiciones de OID permitidos, vea el archivo Wincrypt. h en CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="81c5b-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="81c5b-144">Alto máximo del árbol por debajo de este certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="81c5b-146">Vínculo a la información de la Directiva de la Agencia SPC (por ejemplo, una dirección URL).</span><span class="sxs-lookup"><span data-stu-id="81c5b-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="81c5b-148">Duración del período de validez.</span><span class="sxs-lookup"><span data-stu-id="81c5b-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-149"><strong>-n</strong> <strong>&quot;</strong> <em>Nombre</em> de<strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="81c5b-150">Nombre del certificado del publicador.</span><span class="sxs-lookup"><span data-stu-id="81c5b-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="81c5b-151">Este nombre debe cumplir el estándar <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> .</span><span class="sxs-lookup"><span data-stu-id="81c5b-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="81c5b-152">El método más sencillo es usar el &quot; formato CN =<em>nombre</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="81c5b-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="81c5b-153">Por ejemplo: <strong>-n &quot; CN = test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="81c5b-155">Se debe incluir la extensión de autenticación del cliente de Netscape.</span><span class="sxs-lookup"><span data-stu-id="81c5b-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="81c5b-157">Marca la clave privada como exportable.</span><span class="sxs-lookup"><span data-stu-id="81c5b-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="81c5b-159">Crea un certificado autofirmado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-160"><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="81c5b-161">Nombre del archivo de certificado con la clave pública de asunto existente que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="81c5b-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-162"><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="81c5b-163">Ubicación del contenedor de claves del sujeto que contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>clave privada</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="81c5b-164">Si no existe un contenedor de claves, se creará uno.</span><span class="sxs-lookup"><span data-stu-id="81c5b-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="81c5b-165">Si no se usa la opción <strong>-SK</strong> o <strong>-SV</strong> , se crea un contenedor de claves predeterminado y se utiliza de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81c5b-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-166"><strong>-Sky</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="81c5b-167">Especificación de la clave del sujeto.</span><span class="sxs-lookup"><span data-stu-id="81c5b-167">Subject's key specification.</span></span> <span data-ttu-id="81c5b-168"><em>SubjectKeySpec</em> debe ser uno de los tres valores posibles:</span><span class="sxs-lookup"><span data-stu-id="81c5b-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="81c5b-169"><strong>Signature</strong> (especificación de clave de AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="81c5b-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="81c5b-170"><strong>Exchange</strong> (especificación de clave de AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="81c5b-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="81c5b-171">Un entero, como <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="81c5b-172">Para obtener más información, vea la nota que sigue a esta tabla.</span><span class="sxs-lookup"><span data-stu-id="81c5b-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-173"><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="81c5b-174">Proveedor de CryptoAPI para el sujeto.</span><span class="sxs-lookup"><span data-stu-id="81c5b-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="81c5b-175">El valor predeterminado es el proveedor del usuario.</span><span class="sxs-lookup"><span data-stu-id="81c5b-175">The default is the user's provider.</span></span> <span data-ttu-id="81c5b-176">Para obtener información acerca de los proveedores de CryptoAPI, consulte la documentación de CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="81c5b-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-177"><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="81c5b-178">Ubicación del registro del almacén de certificados del sujeto.</span><span class="sxs-lookup"><span data-stu-id="81c5b-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="81c5b-179"><em>SubjectCertStoreLocation</em> debe ser <strong>LocalMachine</strong> (clave del registro HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (clave del registro HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="81c5b-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="81c5b-180"><strong>CurrentUser</strong> es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-181"><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="81c5b-182">Nombre del almacén de certificados del sujeto en el que se almacenará el certificado generado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-183"><strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="81c5b-184">Nombre del archivo. PVK del sujeto.</span><span class="sxs-lookup"><span data-stu-id="81c5b-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="81c5b-185">Si no se usa la opción <strong>-SK</strong> o <strong>-SV</strong> , se crea un contenedor de claves predeterminado y se utiliza de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81c5b-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-186"><strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="81c5b-187">Tipo de proveedor de CryptoAPI para el asunto.</span><span class="sxs-lookup"><span data-stu-id="81c5b-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="81c5b-188">El valor predeterminado es <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="81c5b-189">Para obtener información sobre los tipos de proveedor de CryptoAPI, vea la documentación de CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="81c5b-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="81c5b-191">Número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-191">Serial number of the certificate.</span></span> <span data-ttu-id="81c5b-192">El valor máximo es 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="81c5b-192">The maximum value is 2^31.</span></span> <span data-ttu-id="81c5b-193">El valor predeterminado es un valor generado por la herramienta que se garantiza que es único.</span><span class="sxs-lookup"><span data-stu-id="81c5b-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="81c5b-195">Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="81c5b-196"><em>CertificateAuthority</em> debe establecerse en <strong>Commercial</strong> (para los certificados que vayan a usar los publicadores de software comercial) o <strong>individual</strong> (para los certificados que vayan a usar los editores de software individuales).</span><span class="sxs-lookup"><span data-stu-id="81c5b-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="81c5b-198">Muestra las opciones básicas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="81c5b-200">Muestra las opciones extendidas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="81c5b-201">Si se usa la opción **-Sky** Key Specification en la versión 4,0 o posterior de Internet Explorer, la especificación debe coincidir con la especificación de clave indicada por el archivo de [*clave privada*](../secgloss/p-gly.md) o el [*contenedor de claves*](../secgloss/k-gly.md)privadas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="81c5b-202">Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="81c5b-203">Si hay más de una especificación de clave en el contenedor de claves, MakeCert primero intentará usar la especificación de la \_ clave at Signature.</span><span class="sxs-lookup"><span data-stu-id="81c5b-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="81c5b-204">Si se produce un error, MakeCert intentará usar en \_ KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="81c5b-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="81c5b-205">Dado que la mayoría de los usuarios tienen una \_ clave at Signature o una \_ clave at KEYEXCHANGE, no es necesario usar esta opción en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="81c5b-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="81c5b-206">Las siguientes opciones son solo para los archivos de [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) y la tecnología de clave privada.</span><span class="sxs-lookup"><span data-stu-id="81c5b-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81c5b-207">SPC y la opción de clave privada</span><span class="sxs-lookup"><span data-stu-id="81c5b-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="81c5b-208">Descripción</span><span class="sxs-lookup"><span data-stu-id="81c5b-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81c5b-209"><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="81c5b-210">Ubicación del certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-211"><strong>-IK</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="81c5b-212">Ubicación del contenedor de claves del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-212">Location of the issuer's key container.</span></span> <span data-ttu-id="81c5b-213">El valor predeterminado es la clave raíz de prueba.</span><span class="sxs-lookup"><span data-stu-id="81c5b-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-214"><strong>-IKY</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="81c5b-215">Especificación de clave del emisor, que debe ser uno de los tres valores posibles:</span><span class="sxs-lookup"><span data-stu-id="81c5b-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="81c5b-216"><strong>Signature</strong> (especificación de clave de AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="81c5b-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="81c5b-217"><strong>Exchange</strong> (especificación de clave de AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="81c5b-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="81c5b-218">Un entero, como <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="81c5b-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="81c5b-219">Para obtener más información, vea la nota que sigue a esta tabla.</span><span class="sxs-lookup"><span data-stu-id="81c5b-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-220"><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="81c5b-221">Proveedor de CryptoAPI para el emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="81c5b-222">El valor predeterminado es el proveedor del usuario.</span><span class="sxs-lookup"><span data-stu-id="81c5b-222">The default is the user's provider.</span></span> <span data-ttu-id="81c5b-223">Para obtener información acerca de los proveedores de CryptoAPI, consulte la documentación de CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="81c5b-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c5b-224"><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="81c5b-225">Archivo de clave privada del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-225">Issuer's private key file.</span></span> <span data-ttu-id="81c5b-226">El valor predeterminado es la raíz de prueba.</span><span class="sxs-lookup"><span data-stu-id="81c5b-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c5b-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="81c5b-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="81c5b-228">Tipo de proveedor de CryptoAPI para el emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="81c5b-229">El valor predeterminado es <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="81c5b-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="81c5b-230">Para obtener información sobre los tipos de proveedor de CryptoAPI, vea la documentación de CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="81c5b-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="81c5b-231">Si se usa la opción **de especificación de clave-IKY** en Internet Explorer 4,0 o posterior, la especificación debe coincidir con la especificación de clave indicada por el archivo de [*clave privada*](../secgloss/p-gly.md) o el [*contenedor de claves*](../secgloss/k-gly.md)privadas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="81c5b-232">Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="81c5b-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="81c5b-233">Si hay más de una especificación de clave en el contenedor de claves, MakeCert primero intentará usar la especificación de la \_ clave at Signature.</span><span class="sxs-lookup"><span data-stu-id="81c5b-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="81c5b-234">Si se produce un error, MakeCert intentará usar en \_ KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="81c5b-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="81c5b-235">Dado que la mayoría de los usuarios tienen una \_ clave at Signature o una \_ clave at KEYEXCHANGE, no es necesario usar esta opción en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="81c5b-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="81c5b-236">Las siguientes opciones son solo para la tecnología de [*almacén de certificados*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="81c5b-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="81c5b-237">Opción de almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="81c5b-237">Certificate store option</span></span>          | <span data-ttu-id="81c5b-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="81c5b-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c5b-239">**-** *IssuerCertFile* IC</span><span class="sxs-lookup"><span data-stu-id="81c5b-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="81c5b-240">Archivo que contiene el certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="81c5b-241">MakeCert buscará un certificado con una coincidencia exacta en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="81c5b-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="81c5b-242">**-en** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="81c5b-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="81c5b-243">Nombre común del certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="81c5b-244">MakeCert buscará en el almacén de certificados un certificado cuyo nombre común incluya *IssuerNameString*.</span><span class="sxs-lookup"><span data-stu-id="81c5b-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="81c5b-245">**-IssuerCertStoreLocation de infrarrojos** </span><span class="sxs-lookup"><span data-stu-id="81c5b-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="81c5b-246">Ubicación del registro del almacén de certificados del emisor.</span><span class="sxs-lookup"><span data-stu-id="81c5b-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="81c5b-247">*IssuerCertStoreLocation* debe ser **LocalMachine** (clave del registro HKEY \_ local \_ Machine) o **CurrentUser** (clave del registro HKEY \_ Current \_ User).</span><span class="sxs-lookup"><span data-stu-id="81c5b-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="81c5b-248">**CurrentUser** es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81c5b-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="81c5b-249">**-es** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="81c5b-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="81c5b-250">Almacén de certificados del emisor que incluye el certificado del emisor y su información de clave privada asociada.</span><span class="sxs-lookup"><span data-stu-id="81c5b-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="81c5b-251">Si hay más de un certificado en el almacén, el usuario debe identificarlo de forma exclusiva mediante la opción **-IC** o **-in** .</span><span class="sxs-lookup"><span data-stu-id="81c5b-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="81c5b-252">Si el certificado del almacén de certificados no se identifica de forma única, se producirá un error en MakeCert.</span><span class="sxs-lookup"><span data-stu-id="81c5b-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
