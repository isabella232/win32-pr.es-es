---
description: La API de inscripción de certificados admite los atributos siguientes. Puede crear un atributo individual mediante la interfaz correspondiente identificada en cada una de las secciones siguientes.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Atributos compatibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774418"
---
# <a name="supported-attributes"></a>Atributos compatibles

La API de inscripción de certificados admite los atributos siguientes. Puede crear un atributo individual mediante la interfaz correspondiente identificada en cada una de las secciones siguientes.

## <a name="clientid"></a>ClientId

La [**interfaz IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) se puede usar para definir un atributo que contiene información sobre el equipo cliente que envió la solicitud de certificado. La información se puede usar para los diagnósticos.

**Se aplica a:** Solicitud PKCS \# 10 o CMC.

**OID:** INFORMACIÓN DE CLIENTE \_ DE SOLICITUD DE OID \_ XCN \_ \_ (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Extensiones

La [**interfaz IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) se puede usar para definir un conjunto de extensiones de certificado X.509 versión 3. Se admiten las siguientes extensiones. Para obtener más información, vea el tema Interfaces de extensión.



| Extensión              | Descripción                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Contiene uno o varios formatos de nombre alternativos del emisor asociado al certificado.                                                                                                                                       |
| AuthorityKeyIdentifier | Contiene un identificador de clave único para diferenciar entre varias claves de firma de certificados de [*la entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA). |
| BasicConstraints       | Indica si el sujeto puede actuar como una entidad de certificación.                                                                                                                                                                                   |
| CertificatePolicies    | Identifica las directivas y la información opcional del calificador asociada al certificado.                                                                                                                                      |
| MSApplicationPolicies  | Identifica uno o varios usos para el certificado. Esta extensión es similar a la extensión EnhancedKeyUsage, pero está definida por Microsoft.                                                                                           |
| EnhancedKeyUsage       | Identifica uno o varios usos de la clave pública contenida en el certificado. La extensión de uso de clave mejorada se puede usar además de o en lugar de la extensión de uso de clave.                                                  |
| KeyUsage               | Identifica restricciones en las operaciones que puede realizar la clave pública contenida en el certificado.                                                                                                                  |
| SmimeCapabilities      | Notifica las funcionalidades de descifrado de un destinatario de correo electrónico al remitente del correo electrónico para permitir que el remitente elija el algoritmo simétrico más seguro admitido por ambas partes.                                                      |
| SubjectKeyIdentifier   | Contiene un identificador de clave único que se puede usar para diferenciar entre varias claves de firma asociadas al propietario del certificado.                                                                                          |
| Plantilla               | Identifica la plantilla que se va a usar al emitir o renovar un certificado. La extensión contiene el identificador de objeto (OID) de la plantilla.                                                                                       |
| TemplateName           | Identifica la plantilla que se va a usar al emitir o renovar un certificado. La extensión contiene el nombre de la plantilla.                                                                                                          |



 

**Se aplica a:** Solicitud PKCS \# 10.

**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>ArchiveKey

La [**interfaz IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) se puede usar para definir un atributo que contiene una clave privada cifrada enviada a una CA para el archivado.

**Se aplica a:** Solicitud de CMC.

**OID:** ATTR DE CLAVE ARCHIVADA DE \_ OID \_ XCN \_ \_ (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

La [**interfaz IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) se puede usar para definir un hash de la clave privada contenida en el **atributo ArchiveKey.**

**Se aplica a:** Solicitud de CMC.

**OID:** XCN \_ OID \_ ENCRYPTED KEY HASH \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>CspProvider

La [**interfaz IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) se puede usar para definir un atributo que contiene información sobre el proveedor de servicios criptográficos [*(CSP)*](/windows/desktop/SecGloss/c-gly) utilizado por el solicitante para las operaciones criptográficas.

**Se aplica a:** Solicitud PKCS \# 10. Este atributo se crea automáticamente al crear un [**objeto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)

**OID:** PROVEEDOR DE CSP DE INSCRIPCIÓN DE OID de XCN \_ \_ \_ \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

La [**interfaz IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) se puede usar para crear un atributo que contiene información de versión sobre el sistema operativo cliente. La entidad de certificación puede usar la información para determinar el tipo de procesamiento que se va a aplicar al crear el certificado.

**Se aplica a:** Solicitud PKCS \# 10 o CMC.

**OID:** XCN \_ OID \_ OS \_ VERSION (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

La [**interfaz IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) se puede usar para crear un atributo que contenga el certificado que se va a renovar.

**Se aplica a:** Solicitud PKCS \# 10. Este atributo se crea automáticamente si crea una solicitud PKCS 10 iniciando con \# el certificado que se va a renovar.

**OID:** CERTIFICADO DE \_ RENOVACIÓN DE OID XCN \_ \_ (1.3.6.1.4.1.311.13.1)

 

 
