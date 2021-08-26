---
description: Puede usar la interfaz IX509Extension para definir una extensión arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensiones admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0362bc289e8f0631520a7d9d56ff4bed1af2c698c721db703b27b0ecee5a1629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101115"
---
# <a name="supported-extensions"></a>Extensiones admitidas

Puede usar la [**interfaz IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir una extensión arbitraria. La API de inscripción de certificados también proporciona interfaces derivadas de **IX509Extension** para permitirle crear fácilmente cualquiera de las extensiones más comunes. En la lista siguiente se identifican las extensiones comunes admitidas por las entidades de certificación de Microsoft y los identificadores de objeto e interfaces que puede usar para crearlas.

## <a name="alternativenames"></a>AlternativeNames

La extensión de nombres alternativos se puede usar para definir uno o varios formularios de nombre alternativos para el sujeto de la solicitud de certificado. Algunos ejemplos de formas alternativas son direcciones de correo electrónico, nombres DNS, direcciones IP y URI.

**Interfaz:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ SUBJECT ALT \_ \_ NAME2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

La extensión de acceso a la información de autoridad identifica cómo acceder a la información y los servicios de ca. El valor de extensión contiene una secuencia de URI.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ AUTHORITY INFO ACCESS \_ \_ (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

La extensión de identificador de clave de entidad de certificación permite la identificación de la clave pública de entidad de certificación que corresponde a la clave privada de la entidad de certificación que firmó un certificado emitido. Lo usa la ruta de acceso del certificado que ejecuta software en Windows servidor para encontrar el certificado de entidad de certificación. Cuando una ca emite un certificado, el valor de extensión se establece igual a la **extensión SubjectKeyIdentifier** en el certificado de firma de ca. El valor suele ser un hash SHA-1 de la clave pública.

**Interfaz:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** XCN \_ OID \_ AUTHORITY KEY \_ \_ IDENTIFIER2 (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

La extensión de restricciones básicas se puede usar para identificar si la entidad se puede usar como entidad de certificación (CA) y, si es así, el número de CA subordinadas que pueden existir debajo de ella en la cadena de certificados.

**Interfaz:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ BASIC \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

La extensión de directivas de certificado se puede usar para identificar las directivas en las que se ha emitido el certificado y se pueden usar los fines para él. Estos se identifican mediante una colección de identificadores de objeto ( IDENTIFICADORES). Las directivas se personalizan según los requisitos de una organización.

**Interfaz:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** DIRECTIVAS DE \_ CERTIFICADO DE OID \_ XCN \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

La extensión de puntos de distribución de lista de revocación de certificados (CRL) contiene el URI de la lista base de revocación de certificados (CRL).

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** PUNTOS DE DISTRIBUCIÓN DE \_ CRL de OID \_ XCN \_ \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

La extensión de uso mejorado de claves se puede usar para definir uno o varios usos de la clave pública contenida en el certificado.

**Interfaz:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** XCN \_ OID \_ ENHANCED KEY USAGE \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

La extensión CRL más reciente contiene el URI de la CRL diferencial. Se usa la misma sintaxis de ASN.1 para esta extensión y la **extensión CrlDistributionPoints.**

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ FRESHEST \_ CRL (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

La extensión de uso de claves se puede usar para definir restricciones en las operaciones que puede realizar la clave pública contenida en el certificado. Por ejemplo, puede especificar que la clave pública solo se utilice para crear una firma digital, firmar una lista de revocación de certificados (CRL) o cifrar otra clave.

**Interfaz:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** USO DE CLAVE \_ DE OID \_ XCN \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

Una aplicación puede usar la extensión de directivas de aplicación de Microsoft para filtrar los certificados en función del uso permitido. Los usos permitidos se identifican mediante ÓID. Esta extensión es similar a la **extensión EnhancedKeyUsage,** pero con una semántica más estricta aplicada a la CA primaria. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** DIRECTIVAS DE CERTIFICADO DE APLICACIÓN OID XCN \_ \_ \_ \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

La extensión de restricciones de nombre se usa para identificar el espacio de nombres en el que deben encontrarse todos los nombres de firmantes de certificados de una jerarquía de certificados. La extensión solo se utiliza en un certificado de CA.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRICCIONES \_ DE NOMBRE DE OID \_ XCN \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

La extensión de restricciones de directiva se agrega a los certificados de entidad de certificación para restringir la validación de rutas de acceso mediante la prohibición de la asignación de directivas o la exigencia de que cada certificado de la jerarquía contenga un identificador de directiva aceptable.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRICCIONES DE \_ DIRECTIVA DE OID \_ XCN \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

La extensión de asignaciones de directivas se usa para identificar las directivas de una CA subordinada que se corresponden con las directivas de la CA emisora. El valor de extensión contiene una secuencia de asignaciones de directivas de CA emisoras y de CA subordinadas representadas por identificadores de objeto.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** ASIGNACIONES DE \_ DIRECTIVAS DE OID \_ XCN \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

La extensión de período de uso de clave privada se usa para especificar un período de validez diferente para la clave privada que para el certificado al que está asociada la clave.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** PERÍODO DE USO DE CLAVE PRIVADA DE OID XCN \_ \_ \_ \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

La extensión de funcionalidades de extensiones de correo electrónico de Internet (S/MIME) seguras o multipropósito se puede usar para notificar las funcionalidades de descifrado de un destinatario de correo electrónico al remitente del mensaje de correo electrónico para que el remitente pueda elegir el algoritmo de cifrado más seguro admitido por ambas partes. El valor de extensión contiene una colección de ESPECIFICACIONES de algoritmos de cifrado simétricos y una seguridad de cifrado opcional para cada uno.

**Interfaz:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

La extensión de atributos de directorio de sujeto se puede usar para transmitir atributos de identificación, como la nacionalidad del sujeto del certificado. El valor de extensión es una secuencia de pares de valores OID.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ SUBJECT DIR \_ \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

La extensión de identificador de clave de sujeto se puede usar para diferenciar entre varias claves públicas que mantiene el sujeto del certificado. El valor de extensión suele ser un hash SHA-1 de la clave.

**Interfaz:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** IDENTIFICADOR DE CLAVE \_ DE ASUNTO DE OID \_ XCN \_ \_ (2.5.29.14)

## <a name="template"></a>Plantilla

La extensión de plantilla se puede usar para identificar la plantilla de la versión 2 que se va a usar al emitir o renovar un certificado. El valor de extensión contiene el OID de plantilla y la información de versión opcional. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** XCN \_ OID \_ CERTIFICATE TEMPLATE \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

La extensión de nombre de plantilla se puede usar para identificar la plantilla de la versión 1 que se va a usar al emitir o renovar un certificado. El valor de extensión contiene el nombre de la plantilla. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** EXTENSIÓN CERTTYPE DE INSCRIPCIÓN DE OID XCN \_ \_ \_ \_ (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensiones](extensions.md)
</dt> </dl>

 

 



