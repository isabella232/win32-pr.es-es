---
description: CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica en todo el sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensiones criptográficas de firmas digitales XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913946"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="3df1f-103">Extensiones criptográficas de firmas digitales XML</span><span class="sxs-lookup"><span data-stu-id="3df1f-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="3df1f-104">CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3df1f-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="3df1f-105">Los archivos dll de extensión amplían los algoritmos que admiten los elementos XML **SignatureMethod** y **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="3df1f-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="3df1f-106">Los archivos dll de extensión pueden admitir algoritmos que codifican parámetros adicionales en la firma digital XML.</span><span class="sxs-lookup"><span data-stu-id="3df1f-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="3df1f-107">Todas las dll de extensiones deben admitir la función [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , que devuelve un puntero a una estructura de [**\_ \_ \_ interfaz criptográfica de XML de cifrado**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) .</span><span class="sxs-lookup"><span data-stu-id="3df1f-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="3df1f-108">Esta estructura proporciona punteros de función a las funciones de extensión criptográfica implementadas.</span><span class="sxs-lookup"><span data-stu-id="3df1f-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="3df1f-109">Las funciones admitidas dependen del tipo de algoritmo criptográfico compatible y de si el algoritmo debe codificar los parámetros en la firma digital XML.</span><span class="sxs-lookup"><span data-stu-id="3df1f-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="3df1f-110">Las funciones de extensiones criptográficas incluyen los siguientes punteros de función:</span><span class="sxs-lookup"><span data-stu-id="3df1f-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="3df1f-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funciones requeridas</span><span class="sxs-lookup"><span data-stu-id="3df1f-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="3df1f-112">**CryptXmlDllGetInterface**</span><span class="sxs-lookup"><span data-stu-id="3df1f-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="3df1f-113">**CryptXmlDllGetAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="3df1f-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="3df1f-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funciones de método de síntesis</span><span class="sxs-lookup"><span data-stu-id="3df1f-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="3df1f-115">**CryptXmlDllCloseDigest**</span><span class="sxs-lookup"><span data-stu-id="3df1f-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="3df1f-116">**CryptXmlDllCreateDigest**</span><span class="sxs-lookup"><span data-stu-id="3df1f-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="3df1f-117">**CryptXmlDllDigestData**</span><span class="sxs-lookup"><span data-stu-id="3df1f-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="3df1f-118">**CryptXmlDllFinalizeDigest**</span><span class="sxs-lookup"><span data-stu-id="3df1f-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="3df1f-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funciones del método Signature</span><span class="sxs-lookup"><span data-stu-id="3df1f-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="3df1f-120">**CryptXmlDllSignData**</span><span class="sxs-lookup"><span data-stu-id="3df1f-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="3df1f-121">**CryptXmlDllVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="3df1f-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="3df1f-122">**CryptXmlDllCreateKey**</span><span class="sxs-lookup"><span data-stu-id="3df1f-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="3df1f-123">**CryptXmlDllEncodeKeyValue**</span><span class="sxs-lookup"><span data-stu-id="3df1f-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="3df1f-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Para los algoritmos con parámetros codificados predeterminados</span><span class="sxs-lookup"><span data-stu-id="3df1f-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="3df1f-125">**CryptXmlDllEncodeAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="3df1f-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="3df1f-126">Los archivos dll de extensión criptográfica se registran en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3df1f-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="3df1f-127">Se requieren privilegios de administrador para registrar un archivo DLL de extensión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="3df1f-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="3df1f-128">Todas las extensiones criptográficas de CryptXML se registran mediante el valor de URI establecido en el campo **SignatureMethod** o el atributo Algorithm del elemento **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="3df1f-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="3df1f-129">Las rutas de acceso del registro para los archivos dll de extensión son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="3df1f-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="3df1f-130"><span id="32-bit"></span><span id="32-BIT"></span>32 bits</span><span class="sxs-lookup"><span data-stu-id="3df1f-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="3df1f-131">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="3df1f-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="3df1f-132"><span id="64-bit"></span><span id="64-BIT"></span>64 bits</span><span class="sxs-lookup"><span data-stu-id="3df1f-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="3df1f-133">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="3df1f-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="3df1f-134">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="3df1f-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="3df1f-135">Cada clave contiene la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="3df1f-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3df1f-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="3df1f-136">Name</span></span></th>
<th><span data-ttu-id="3df1f-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="3df1f-137">Type</span></span></th>
<th><span data-ttu-id="3df1f-138">Datos</span><span class="sxs-lookup"><span data-stu-id="3df1f-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3df1f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3df1f-139">DLL</span></span><br/></td>
<td><span data-ttu-id="3df1f-140">Cadena expansible</span><span class="sxs-lookup"><span data-stu-id="3df1f-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="3df1f-141">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3df1f-141">Required.</span></span><br/><span data-ttu-id="3df1f-142">Ruta de acceso absoluta al archivo DLL del proveedor de servicios criptográficos XML.</span><span class="sxs-lookup"><span data-stu-id="3df1f-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="3df1f-143"><b>Nota: </b> Se recomienda que los archivos dll de extensión criptográfica se encuentren en directorios en los que solo puedan escribir las aplicaciones con privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="3df1f-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="3df1f-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> se usa para cargar el archivo dll de extensión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="3df1f-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3df1f-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="3df1f-145">Name</span></span><br/></td>
<td><span data-ttu-id="3df1f-146"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3df1f-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="3df1f-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3df1f-147">Optional.</span></span><br/> <span data-ttu-id="3df1f-148">El nombre para mostrar asociado con este URI.</span><span class="sxs-lookup"><span data-stu-id="3df1f-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3df1f-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="3df1f-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="3df1f-150"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3df1f-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="3df1f-151">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3df1f-151">Required.</span></span><br/> <span data-ttu-id="3df1f-152">Identificador de grupo asociado a este algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="3df1f-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="3df1f-153">Entre los valores posibles se incluyen los siguientes:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="3df1f-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="3df1f-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="3df1f-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3df1f-155">CNGAlgid</span><span class="sxs-lookup"><span data-stu-id="3df1f-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="3df1f-156"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3df1f-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="3df1f-157">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3df1f-157">Required.</span></span><br/> <span data-ttu-id="3df1f-158">Nombre del algoritmo CNG que se va a pasar a las funciones BCrypt o NCrypt.</span><span class="sxs-lookup"><span data-stu-id="3df1f-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3df1f-159">CNGExtraAlgid</span><span class="sxs-lookup"><span data-stu-id="3df1f-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="3df1f-160"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3df1f-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="3df1f-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3df1f-161">Optional.</span></span><br/> <span data-ttu-id="3df1f-162">Una cadena de algoritmo adicional, que no sea la cadena en el miembro CNGAlgid, que se puede pasar a las funciones de CNG.</span><span class="sxs-lookup"><span data-stu-id="3df1f-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="3df1f-163">Para los algoritmos de firma (CRYPT_XML_GROUP_ID_SIGN), este miembro es la cadena de algoritmo de clave pública que se va a pasar a las funciones de CNG.</span><span class="sxs-lookup"><span data-stu-id="3df1f-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="3df1f-164">Para los demás valores de GroupId, establezca el miembro <strong>pwszCNGExtraAlgid</strong> en la cadena vacía, L &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="3df1f-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3df1f-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3df1f-165">Related topics</span></span>

<dl> <span data-ttu-id="3df1f-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3df1f-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="3df1f-167">Algoritmos criptográficos de firma digital XML</span><span class="sxs-lookup"><span data-stu-id="3df1f-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
