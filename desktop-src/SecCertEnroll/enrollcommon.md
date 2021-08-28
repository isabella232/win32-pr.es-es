---
description: La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos proporcionados con el SDK de inscripción de certificados.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476021"
---
# <a name="enrollcommon"></a>enrollCommon

La carpeta enrollCommon contiene las siguientes funciones auxiliares y macros usadas por los ejemplos proporcionados con el SDK de inscripción de certificados. Se instala de forma predeterminada en la carpeta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon .




| Función | Descripción | 
|----------|-------------|
| _JumpIfError | Macro que acepta un <strong>valor HRESULT,</strong> una etiqueta y una cadena de error, imprime la cadena y transfiere el control de programa a la primera instrucción que sigue a la etiqueta. | 
| _JumpError | Igual que la _JumpIfError macro. | 
| _PrintIfError | No se usa actualmente. | 
| _PrintError | Macro que imprime un mensaje de error y un <strong>valor HRESULT.</strong> | 
| convertWszToSz | Convierte una cadena de caracteres anchos en una cadena de caracteres ASCII mediante la función <strong>WideCharToMultiByte</strong> y el identificador de página de códigos ANSI actual del sistema. Las funciones decConvertFromUnicode y findOIDFromTemplateName definidas en enrollCommon.cpp usan esta función. | 
| convertSzToWsz | Convierte una cadena ASCII en una cadena de caracteres anchos mediante la función <strong>MultiByteToWideChar</strong> y el identificador de página de códigos ANSI actual del sistema. Esta función la usa la función findCertByTemplate definida en enrollCommon.cpp. | 
| convertSzToBstr | Convierte una cadena ASCII en <strong>un BSTR</strong> mediante la <strong>función MultiByteToWideChar.</strong> Esta función no se usa actualmente. | 
| convertWszToBstr | Convierte una cadena de caracteres anchos en <strong>un BSTR</strong>. El ejemplo installResponseFromPFX usa esta función. | 
| checkEnrollStatus | Comprueba el estado del proceso de inscripción de certificados mediante las interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Esta función se usa en los ejemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert. | 
| findCertByKeyUsage | Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que el uso previsto de la clave pública coincide con un valor especificado. El valor especificado puede ser una combinación bit a bit de las marcas siguientes:<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>El ejemplo enrollFromPublicKey usa esta función.<br /> | 
| findCertByEKU | Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que la extensión Uso mejorado de clave (EKU) coincide con la especificada en la entrada. Para obtener más información sobre la extensión EKU, vea la <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>interfaz IX509ExtensionEnhancedKeyUsage.</strong></a> El ejemplo enrollEOBOCMC usa esta función. | 
| findCertByTemplate | Enumera el almacén de certificados personal del usuario actual para buscar el primer certificado para el que la plantilla coincide con el especificado, por nombre, en la entrada. Los ejemplos enrollPKCS7 e enrollRenewalPKCS7 usan esta función. | 
| enrollCertByTemplate | Inicializa un objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> mediante una plantilla, intenta inscribir la solicitud de certificado creada implícitamente y supervisa el estado del proceso de inscripción. Los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7 usan esta función. | 
| verifyCertContext | Comprueba el cumplimiento de la cadena de certificados con la directiva (base) especificada y, opcionalmente, con una extensión de uso mejorado de claves (EKU) especificada. Para obtener más información, vea <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>la función CertVerifyCertificateChainPolicy</strong></a> y las <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> y <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> estructuras. Los ejemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7 usan esta función. | 
| decConvertFromUnicode | Convierte una cadena de caracteres Unicode de doble byte en una cadena de caracteres ANSI de un solo byte. Esta función la usa la función DecodeFileW definida en enrollCommon.cpp. | 
| DecodeFileW | Descodifica un certificado codificado o un archivo de solicitud de certificado en una matriz de bytes. El ejemplo installResponseFromPFX usa esta función. | 
| EncodeToFileW | Codifica un certificado o una solicitud de certificado y lo guarda en un archivo. Esta función se usa en los ejemplos createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey. | 
| findOIDFromTemplateName | Recupera el identificador de objeto de una plantilla especificada por nombre. Esta función la usa la función findCertByTemplate definida en enrollCommon.cpp. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

