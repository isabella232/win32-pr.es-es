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
# <a name="enrollcommon"></a>enrollCommon

La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos que se proporcionan con el SDK de inscripción de certificados. Se instala de forma predeterminada en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCommon



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Macro que acepta un valor <strong>HRESULT</strong> , una etiqueta y una cadena de error, imprime la cadena y transfiere el control del programa a la primera instrucción que sigue a la etiqueta.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Igual que la macro _JumpIfError.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>No se usa actualmente.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Macro que imprime un mensaje de error y un valor <strong>HRESULT</strong> .</td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Convierte una cadena de caracteres anchos en una cadena de caracteres ASCII mediante la función <strong>WideCharToMultiByte</strong> y el identificador de página de códigos ANSI actual del sistema. Esta función la usan las funciones decConvertFromUnicode y findOIDFromTemplateName definidas en enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Convierte una cadena ASCII en una cadena de caracteres anchos mediante la función <strong>MultiByteToWideChar</strong> y el identificador de página de códigos ANSI actual del sistema. Esta función se usa en la función findCertByTemplate definida en enrollCommon. cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Convierte una cadena ASCII en un <strong>BSTR</strong> mediante la función <strong>MultiByteToWideChar</strong> . Esta función no se usa actualmente.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Convierte una cadena de caracteres anchos en un <strong>BSTR</strong>. Esta función se usa en el ejemplo installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Comprueba el estado del proceso de inscripción de certificados mediante el uso de las interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Esta función se usa en los ejemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert y enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado para el que el uso previsto de la clave pública coincide con un valor especificado. El valor especificado puede ser una combinación bit a bit de las marcas siguientes:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Esta función se usa en el ejemplo enrollFromPublicKey.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado cuya extensión de uso mejorado de clave (EKU) coincide con la especificada en la entrada. Para obtener más información sobre la extensión EKU, vea la interfaz <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Esta función se usa en el ejemplo enrollEOBOCMC.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumera el almacén de certificados personales del usuario actual para buscar el primer certificado para el que la plantilla coincide con el especificado, por nombre, en la entrada. Esta función se usa en los ejemplos enrollPKCS7 y enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Inicializa un objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> mediante una plantilla, intenta inscribir la solicitud de certificado creada implícitamente y supervisa el estado del proceso de inscripción. Esta función se usa en los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 y enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Comprueba la compatibilidad de la cadena de certificados con la Directiva especificada (base) y, opcionalmente, con una extensión de uso mejorado de clave (EKU) especificado. Para obtener más información, vea la función <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> y las estructuras <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> y <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Esta función se usa en los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 y enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Convierte una cadena de caracteres Unicode de doble byte en una cadena de caracteres ANSI de un solo byte. Esta función se usa en la función DecodeFileW definida en enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Descodifica un certificado codificado o un archivo de solicitud de certificado en una matriz de bytes. Esta función se usa en el ejemplo installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Codifica un certificado o una solicitud de certificado y lo guarda en un archivo. Esta función se usa en los ejemplos createCNGCustomCMC, enrollEOBOCMC y enrollFromPublicKey.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Recupera el identificador de objeto de una plantilla especificada por el nombre. Esta función se usa en la función findCertByTemplate definida en enrollCommon. cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

