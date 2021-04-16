---
description: La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos que se proporcionan con el SDK de inscripción de certificados.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542691"
---
# <a name="enrollcommon"></a><span data-ttu-id="42c54-103">enrollCommon</span><span class="sxs-lookup"><span data-stu-id="42c54-103">enrollCommon</span></span>

<span data-ttu-id="42c54-104">La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos que se proporcionan con el SDK de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="42c54-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="42c54-105">Se instala de forma predeterminada en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCommon</span><span class="sxs-lookup"><span data-stu-id="42c54-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42c54-106">Función</span><span class="sxs-lookup"><span data-stu-id="42c54-106">Function</span></span></th>
<th><span data-ttu-id="42c54-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="42c54-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42c54-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="42c54-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="42c54-109">Macro que acepta un valor <strong>HRESULT</strong> , una etiqueta y una cadena de error, imprime la cadena y transfiere el control del programa a la primera instrucción que sigue a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="42c54-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="42c54-110">_JumpError</span></span></td>
<td><span data-ttu-id="42c54-111">Igual que la macro _JumpIfError.</span><span class="sxs-lookup"><span data-stu-id="42c54-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="42c54-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="42c54-113">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="42c54-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="42c54-114">_PrintError</span></span></td>
<td><span data-ttu-id="42c54-115">Macro que imprime un mensaje de error y un valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="42c54-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-116">convertWszToSz</span><span class="sxs-lookup"><span data-stu-id="42c54-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="42c54-117">Convierte una cadena de caracteres anchos en una cadena de caracteres ASCII mediante la función <strong>WideCharToMultiByte</strong> y el identificador de página de códigos ANSI actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="42c54-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="42c54-118">Esta función la usan las funciones decConvertFromUnicode y findOIDFromTemplateName definidas en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="42c54-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-119">convertSzToWsz</span><span class="sxs-lookup"><span data-stu-id="42c54-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="42c54-120">Convierte una cadena ASCII en una cadena de caracteres anchos mediante la función <strong>MultiByteToWideChar</strong> y el identificador de página de códigos ANSI actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="42c54-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="42c54-121">Esta función se usa en la función findCertByTemplate definida en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="42c54-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-122">convertSzToBstr</span><span class="sxs-lookup"><span data-stu-id="42c54-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="42c54-123">Convierte una cadena ASCII en un <strong>BSTR</strong> mediante la función <strong>MultiByteToWideChar</strong> .</span><span class="sxs-lookup"><span data-stu-id="42c54-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="42c54-124">Esta función no se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="42c54-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-125">convertWszToBstr</span><span class="sxs-lookup"><span data-stu-id="42c54-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="42c54-126">Convierte una cadena de caracteres anchos en un <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="42c54-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="42c54-127">Esta función se usa en el ejemplo installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="42c54-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-128">checkEnrollStatus</span><span class="sxs-lookup"><span data-stu-id="42c54-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="42c54-129">Comprueba el estado del proceso de inscripción de certificados mediante el uso de las interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="42c54-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="42c54-130">Esta función se usa en los ejemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert y enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="42c54-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-131">findCertByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="42c54-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="42c54-132">Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado para el que el uso previsto de la clave pública coincide con un valor especificado.</span><span class="sxs-lookup"><span data-stu-id="42c54-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="42c54-133">El valor especificado puede ser una combinación bit a bit de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="42c54-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="42c54-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="42c54-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="42c54-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="42c54-141">Esta función se usa en el ejemplo enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="42c54-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-142">findCertByEKU</span><span class="sxs-lookup"><span data-stu-id="42c54-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="42c54-143">Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado cuya extensión de uso mejorado de clave (EKU) coincide con la especificada en la entrada.</span><span class="sxs-lookup"><span data-stu-id="42c54-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="42c54-144">Para obtener más información sobre la extensión EKU, vea la interfaz <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="42c54-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="42c54-145">Esta función se usa en el ejemplo enrollEOBOCMC.</span><span class="sxs-lookup"><span data-stu-id="42c54-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-146">findCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="42c54-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="42c54-147">Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado para el que la plantilla coincide con el especificado, por nombre, en la entrada.</span><span class="sxs-lookup"><span data-stu-id="42c54-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="42c54-148">Esta función se usa en los ejemplos enrollPKCS7 y enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="42c54-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-149">enrollCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="42c54-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="42c54-150">Inicializa un objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> mediante una plantilla, intenta inscribir la solicitud de certificado creada implícitamente y supervisa el estado del proceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="42c54-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="42c54-151">Esta función se usa en los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 y enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="42c54-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-152">verifyCertContext</span><span class="sxs-lookup"><span data-stu-id="42c54-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="42c54-153">Comprueba la compatibilidad de la cadena de certificados con la Directiva especificada (base) y, opcionalmente, con una extensión de uso mejorado de clave (EKU) especificado.</span><span class="sxs-lookup"><span data-stu-id="42c54-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="42c54-154">Para obtener más información, vea la función <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> y las estructuras <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> y <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="42c54-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="42c54-155">Esta función se usa en los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 y enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="42c54-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-156">decConvertFromUnicode</span><span class="sxs-lookup"><span data-stu-id="42c54-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="42c54-157">Convierte una cadena de caracteres Unicode de doble byte en una cadena de caracteres ANSI de un solo byte.</span><span class="sxs-lookup"><span data-stu-id="42c54-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="42c54-158">Esta función se usa en la función DecodeFileW definida en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="42c54-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-159">DecodeFileW</span><span class="sxs-lookup"><span data-stu-id="42c54-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="42c54-160">Descodifica un certificado codificado o un archivo de solicitud de certificado en una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="42c54-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="42c54-161">Esta función se usa en el ejemplo installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="42c54-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42c54-162">EncodeToFileW</span><span class="sxs-lookup"><span data-stu-id="42c54-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="42c54-163">Codifica un certificado o una solicitud de certificado y lo guarda en un archivo.</span><span class="sxs-lookup"><span data-stu-id="42c54-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="42c54-164">Esta función se usa en los ejemplos createCNGCustomCMC, enrollEOBOCMC y enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="42c54-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42c54-165">findOIDFromTemplateName</span><span class="sxs-lookup"><span data-stu-id="42c54-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="42c54-166">Recupera el identificador de objeto de una plantilla especificada por el nombre.</span><span class="sxs-lookup"><span data-stu-id="42c54-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="42c54-167">Esta función se usa en la función findCertByTemplate definida en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="42c54-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="42c54-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42c54-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42c54-169">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="42c54-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

