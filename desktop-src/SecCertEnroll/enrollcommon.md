---
description: La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos proporcionados con el SDK de inscripción de certificados.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d087ce1aeced0ef68f5b33a06546897d09687ae5ccbd096f1bb34552d0a4a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780074"
---
# <a name="enrollcommon"></a>enrollCommon

La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos proporcionados con el SDK de inscripción de certificados. Se instala de forma predeterminada en la carpeta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon .



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
<td>Macro que acepta un <strong>valor HRESULT,</strong> una etiqueta y una cadena de error, imprime la cadena y transfiere el control de programa a la primera instrucción que sigue a la etiqueta.</td>
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
<td>Macro que imprime un mensaje de error y un <strong>valor HRESULT.</strong></td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Convierte una cadena de caracteres anchos en una cadena de caracteres ASCII mediante la función <strong>WideCharToMultiByte</strong> y el identificador de página de códigos ANSI actual del sistema. Las funciones decConvertFromUnicode y findOIDFromTemplateName definidas en enrollCommon.cpp usan esta función.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Convierte una cadena ASCII en una cadena de caracteres anchos mediante la función <strong>MultiByteToWideChar</strong> y el identificador de página de códigos ANSI actual del sistema. Esta función la usa la función findCertByTemplate definida en enrollCommon.cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Convierte una cadena ASCII en <strong>un BSTR</strong> mediante la <strong>función MultiByteToWideChar.</strong> Esta función no se usa actualmente.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Convierte una cadena de caracteres anchos en <strong>un BSTR</strong>. El ejemplo installResponseFromPFX usa esta función.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Comprueba el estado del proceso de inscripción de certificados mediante las interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Esta función se usa en los ejemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que el uso previsto de la clave pública coincide con un valor especificado. El valor especificado puede ser una combinación bit a bit de las marcas siguientes:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
El ejemplo enrollFromPublicKey usa esta función.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que la extensión Uso mejorado de clave (EKU) coincide con la especificada en la entrada. Para obtener más información sobre la extensión EKU, vea la <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>interfaz IX509ExtensionEnhancedKeyUsage.</strong></a> El ejemplo enrollEOBOCMC usa esta función.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que la plantilla coincide con el especificado, por nombre, en la entrada. Los ejemplos enrollPKCS7 e enrollRenewalPKCS7 usan esta función.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Inicializa un objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> mediante una plantilla, intenta inscribir la solicitud de certificado creada implícitamente y supervisa el estado del proceso de inscripción. Los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7 usan esta función.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Comprueba el cumplimiento de la cadena de certificados con la directiva (base) especificada y, opcionalmente, con una extensión de uso mejorado de claves (EKU) especificada. Para obtener más información, vea <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>la función CertVerifyCertificateChainPolicy</strong></a> y las <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> y <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> estructuras. Los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7 usan esta función.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Convierte una cadena de caracteres Unicode de doble byte en una cadena de caracteres ANSI de un solo byte. Esta función la usa la función DecodeFileW definida en enrollCommon.cpp.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Descodifica un certificado codificado o un archivo de solicitud de certificado en una matriz de bytes. El ejemplo installResponseFromPFX usa esta función.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Codifica un certificado o una solicitud de certificado y lo guarda en un archivo. Esta función la usan los ejemplos createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Recupera el identificador de objeto de una plantilla especificada por nombre. Esta función la usa la función findCertByTemplate definida en enrollCommon.cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

