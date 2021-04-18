---
description: Se pueden usar las siguientes interfaces para crear extensiones de certificado.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Interfaces de extensión de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541803"
---
# <a name="certificate-extension-interfaces"></a>Interfaces de extensión de certificados

Se pueden usar las siguientes interfaces para crear extensiones de certificado.



| Interfaz                                                                            | Descripción                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Representa una instancia de una extensión **AlternativeNames** .                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Administra una colección de objetos [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) .                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Especifica una directiva de certificado que identifica el propósito para el que se puede utilizar el certificado.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Administra una colección de objetos [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) .                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Representa un calificador que se puede asociar a una directiva de certificado.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Administra una colección de objetos [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) .                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Define una extensión para una solicitud de certificado.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Especifica una o varias formas de nombre alternativo para el firmante de un certificado.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Representa una extensión **AuthorityKeyIdentifier** .                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Especifica si el sujeto del certificado es una entidad de certificación y, en caso afirmativo, la profundidad de la cadena de entidad de certificación subordinada. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Representa una colección de términos de información de directiva.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Representa una colección de identificadores de objeto que indican el modo en que una aplicación puede utilizar un certificado.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Representa una colección de identificadores de objetos que identifican los usos previstos de la clave pública contenida en un certificado.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Representa las restricciones de las operaciones que puede realizar la clave pública incluida en el certificado.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Administra una colección de objetos [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Representa una colección que notifica las capacidades de descifrado de un destinatario de correo electrónico a un remitente de correo electrónico.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Representa una extensión **SubjectKeyIdentifier** usada para identificar un certificado de firma.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Representa una extensión **CertificateTemplate** que contiene una plantilla de la versión 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Representa una extensión **CertificateTemplateName** que contiene una plantilla de la versión 1.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Administra una colección de objetos [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) .                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Representa una extensión **SMIMECapabilities** que identifica las capacidades de descifrado de un destinatario de correo electrónico.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



