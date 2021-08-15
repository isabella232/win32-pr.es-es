---
description: Las interfaces siguientes se pueden usar para crear extensiones de certificado.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Interfaces de extensión de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d254a413331e1f8bc1da630911258d8e327f000d10003c11b784856cd88e84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902736"
---
# <a name="certificate-extension-interfaces"></a>Interfaces de extensión de certificado

Las interfaces siguientes se pueden usar para crear extensiones de certificado.



| Interfaz                                                                            | Descripción                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Representa una instancia de una **extensión AlternativeNames.**                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Administra una colección de [**objetos IAlternativeName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Especifica una directiva de certificado que identifica el propósito para el que se puede usar el certificado.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Administra una colección de [**objetos ICertificatePolicy.**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Representa un calificador que se puede asociar a una directiva de certificado.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Administra una colección de [**objetos IPolicyQualifier.**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Define una extensión para una solicitud de certificado.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Especifica uno o varios formularios de nombre alternativos para el firmantes de un certificado.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Representa una **extensión AuthorityKeyIdentifier.**                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Especifica si el sujeto del certificado es una entidad de certificación y, si es así, la profundidad de la cadena de entidades de certificación subordinadas. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Representa una colección de términos de información de directiva.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Representa una colección de identificadores de objeto que indican cómo una aplicación puede usar un certificado.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Representa una colección de identificadores de objeto que identifican los usos previstos de la clave pública contenida en un certificado.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Representa restricciones en las operaciones que puede realizar la clave pública contenida en el certificado.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Administra una colección de [**objetos IX509Extension.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Representa una colección que notifica las funcionalidades de descifrado de un destinatario de correo electrónico a un remitente de correo electrónico.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Representa una **extensión SubjectKeyIdentifier** que se usa para identificar un certificado de firma.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Representa una **extensión CertificateTemplate** que contiene una plantilla de versión 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Representa una **extensión CertificateTemplateName** que contiene una plantilla de versión 1.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Administra una colección de [**objetos ISmimeCapability.**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Representa una **extensión SMIMECapabilities** que identifica las funcionalidades de descifrado de un destinatario de correo electrónico.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



