---
description: Puede usar la interfaz IX509Extension para definir una extensión arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensiones admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810273"
---
# <a name="supported-extensions"></a>Extensiones admitidas

Puede usar la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir una extensión arbitraria. La API de inscripción de certificados también proporciona interfaces derivadas de **IX509Extension** para que pueda crear fácilmente cualquiera de las extensiones más comunes. En la lista siguiente se identifican las extensiones comunes que admiten las entidades de certificación de Microsoft, así como los identificadores de objeto e interfaces que se pueden usar para crearlas.

## <a name="alternativenames"></a>AlternativeNames

La extensión de nombres alternativos se puede usar para definir una o varias formas de nombres alternativos para el sujeto de la solicitud de certificado. Algunos ejemplos de formas alternativas son direcciones de correo electrónico, nombres DNS, direcciones IP y URI.

**Interfaz:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ Subject \_ ALT \_ nombre2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

La extensión de acceso a la información de entidad de certificación identifica cómo obtener acceso a la información y los servicios de CA. El valor de extensión contiene una secuencia de URI.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Authority \_ \_ Access Info Access (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

La extensión de identificador de clave de entidad de certificación habilita la identificación de la clave pública de CA correspondiente a la clave privada de CA que firmó un certificado emitido. Lo usa la creación de rutas de acceso de certificado en un servidor de Windows para buscar el certificado de CA. Cuando una CA emite un certificado, el valor de la extensión se establece igual a la extensión **SubjectKeyIdentifier** en el certificado de firma de la entidad de certificación. Normalmente, el valor es un hash SHA-1 de la clave pública.

**Interfaz:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** XCN \_ OID \_ Authority \_ key \_ identificador2 (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

La extensión de restricciones básicas se puede usar para identificar si la entidad se puede usar como entidad de certificación (CA) y, si es así, el número de CA subordinadas que pueden existir debajo de ella en la cadena de certificados.

**Interfaz:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

La extensión de directivas de certificados se puede usar para identificar las directivas en las que se ha emitido el certificado y se pueden usar los propósitos para ello. Se identifican mediante una colección de identificadores de objeto (OID). Las directivas se personalizan para los requisitos de una organización.

**Interfaz:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** XCN \_ \_ directivas de certificado OID \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

La extensión de puntos de distribución de lista de revocación de certificados (CRL) contiene el URI de la lista de revocación de certificados (CRL) base.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Puntos de distribución de CRL de XCN \_ OID \_ \_ \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>Campo EnhancedKeyUsage

La extensión uso mejorado de clave se puede usar para definir uno o más usos de la clave pública incluida en el certificado.

**Interfaz:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** \_Uso mejorado de clave de XCN OID \_ \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

La extensión CRL más reciente contiene el URI de la CRL delta. Se usa la misma sintaxis ASN. 1 para esta extensión y la extensión **CrlDistributionPoints** .

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** CRL más reciente de XCN \_ OID \_ \_ (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

La extensión uso de clave se puede usar para definir restricciones en las operaciones que puede realizar la clave pública incluida en el certificado. Por ejemplo, puede especificar que la clave pública se use solo para crear una firma digital, firmar una lista de revocación de certificados (CRL) o cifrar otra clave.

**Interfaz:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** Uso de la \_ clave XCN OID \_ \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

Una aplicación puede usar la extensión de directivas de aplicación de Microsoft para filtrar los certificados en función del uso permitido. Los usos permitidos se identifican mediante OID. Esta extensión es similar a la extensión **campo EnhancedKeyUsage** , pero con una semántica más estricta aplicada a la CA primaria. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** \_Directivas de certificados de aplicación XCN OID \_ \_ \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

La extensión de restricciones de nombres se usa para identificar el espacio de nombres en el que se deben encontrar todos los nombres de asunto de los certificados en una jerarquía de certificados. La extensión solo se utiliza en un certificado de CA.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRICCIONES de nombre de OID de XCN \_ \_ \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

La extensión de restricciones de Directiva se agrega a los certificados de CA para restringir la validación de la ruta de acceso mediante la prohibición de la asignación de directivas o la exigencia de que cada certificado de la jerarquía contenga un identificador de directiva aceptable.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRICCIONES de la \_ Directiva XCN OID \_ \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

La extensión de asignaciones de directivas se usa para identificar las directivas de una CA subordinada que se corresponden con las directivas de la CA emisora. El valor de extensión contiene una secuencia de asignaciones de CA emisora y de directiva de CA subordinada representadas por identificadores de objeto.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Asignaciones de directivas de XCN \_ OID \_ \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

La extensión de período de uso de clave privada se utiliza para especificar un período de validez diferente para la clave privada que para el certificado al que está asociada la clave.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ PRIVATEKEY \_ período de uso \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

La extensión de funciones de extensiones seguras multipropósito de correo Internet (S/MIME) se puede usar para notificar las funciones de descifrado de un destinatario de correo electrónico al remitente del mensaje de correo electrónico para que el remitente pueda elegir el algoritmo de cifrado más seguro compatible con ambas partes. El valor de extensión contiene una colección de OID de algoritmo de cifrado simétrico y una seguridad de cifrado opcional para cada uno.

**Interfaz:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

La extensión de atributos de directorio de asunto se puede usar para transmitir atributos de identificación, como la nacionalidad del firmante del certificado. El valor de extensión es una secuencia de pares de valores OID.

**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID de \_ objeto de firmante \_ \_ (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

La extensión del identificador de clave de sujeto se puede usar para diferenciar entre varias claves públicas retenidas por el sujeto del certificado. El valor de extensión suele ser un hash SHA-1 de la clave.

**Interfaz:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** Identificador de clave de sujeto de XCN \_ OID \_ \_ \_ (2.5.29.14)

## <a name="template"></a>Plantilla

La extensión de plantilla se puede usar para identificar la plantilla de la versión 2 que se va a usar al emitir o renovar un certificado. El valor de la extensión contiene el OID de la plantilla y la información de versión opcional. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** XCN \_ \_ plantilla de certificado OID \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

La extensión de nombre de plantilla se puede usar para identificar la plantilla de la versión 1 que se va a usar al emitir o renovar un certificado. El valor de la extensión contiene el nombre de la plantilla. La extensión es específica de Microsoft.

**Interfaz:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** XCN \_ OID \_ ENROLL \_ CERTTYPE \_ Extension (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensiones](extensions.md)
</dt> </dl>

 

 



