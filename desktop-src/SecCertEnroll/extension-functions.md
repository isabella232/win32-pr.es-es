---
description: El formato de certificado X. 509 versión 3 identifica varias extensiones que se pueden agregar a un certificado para proporcionar información mejorada sobre el uso de claves, directivas de certificados y restricciones, formas de nombres alternativos, etc.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Funciones de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc490c8763a00fae9e7fb1e8a702ff87e2c18fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688048"
---
# <a name="extension-functions"></a>Funciones de extensión

El formato de certificado [*X. 509*](/windows/desktop/SecGloss/x-gly) versión 3 identifica varias extensiones que se pueden agregar a un certificado para proporcionar información mejorada sobre el uso de claves, directivas de certificados y restricciones, formas de nombres alternativos, etc.

CertEnroll.dll implementa las siguientes interfaces para administrar las extensiones de certificado:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar las extensiones de certificado. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas:

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Temas relacionados](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

La función [**AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) de Xenroll.dll agrega una plantilla de certificado, por nombre, a una solicitud.

Con CertEnroll.dll, el método preferido para incorporar una plantilla en una solicitud de certificado es usar el método [**InitializeFromTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) en un \# objeto de solicitud PKCS 10 o [* PKCS) o el método [**INITIALIZEFROMINNERREQUESTTEMPLATENAME**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) en una solicitud CMC.

Si una plantilla específica no está disponible en el cliente, pero se espera que sea entendida por la [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA), puede usar la interfaz [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) para agregar una plantilla de la versión 1 o puede usar la interfaz [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) para agregar una plantilla de la versión 2 a una solicitud de certificado. Por ejemplo, para agregar una plantilla de la versión 1, realice las siguientes acciones:

1.  Cree un objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Cree un objeto [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) y llame al método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) , especificando el nombre de la plantilla.
3.  Agregue la extensión creada a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) llamando al método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Cree un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) y llame al método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , especificando la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en la entrada.
5.  Recupere un objeto de colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) llamando a la propiedad [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) en un objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

La función [**AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) de Xenroll.dll agrega una plantilla de certificado a una solicitud por nombre, identificador de objeto y versión.

Para obtener información sobre cómo usar CertEnroll.dll para incorporar información de plantilla en una solicitud, vea AddCertTypeToRequestWStr.

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

La función [**AddExtensionsToRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) de Xenroll.dll agrega una colección de extensiones a una solicitud.

En CertEnroll.dll, las extensiones se agregan a la colección de atributos de una solicitud CMC o PKCS \# 10. Para agregar extensiones, realice las siguientes acciones:

1.  Cree un objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Cree un objeto [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) y llame al método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) para crear una extensión a partir de un identificador de objeto y un valor de extensión, o use cualquiera de las interfaces enumeradas anteriormente para definir una de las extensiones más comunes.
3.  Agregue cada nueva extensión creada en el paso anterior a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) llamando al método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

La función [**addExtensionToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) de Xenroll.dll agrega una extensión específica a la solicitud.

En CertEnroll.dll, se debe definir una extensión específica y agregarla a una colección de extensiones antes de que se agregue la colección de extensiones a la colección de atributos de una solicitud CMC o PKCS \# 10. Para obtener más información, vea la explicación de AddExtensionsToRequest anterior.

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

La función [**EnableSMIMECapabilities**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) de Xenroll.dll especifica o recupera un valor booleano que indica si se va a agregar la extensión **SMIMECapabilities** a la solicitud.

Puede llamar a la propiedad [**SmimeCapabilities**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) del objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para agregar automáticamente un objeto [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) a la solicitud antes de la codificación.

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

La función [**IncludeSubjectKeyID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) de Xenroll.dll especifica o recupera un valor booleano que indica si se va a agregar la extensión **SubjectKeyIdentifier** a la solicitud.

De forma predeterminada, la extensión **SubjectKeyIdentifier** se crea cuando se inicializa el objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . Puede invalidar este comportamiento llamando a la propiedad [**SuppressOids**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) .

Si tiene un [*par de claves pública y privada*](/windows/desktop/SecGloss/p-gly), también puede usar la interfaz [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) en CertEnroll.dll para agregar una extensión **SubjectKeyIdentifier** a una solicitud de certificado mediante la realización de las siguientes acciones:

1.  Cree un objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Cree un objeto [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) y llame al método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) , especificando una cadena que contiene el identificador. Normalmente, es un hash SHA-1 de 20 bytes de la [*clave pública*](/windows/desktop/SecGloss/p-gly) incluida en el certificado de firma de la entidad de certificación.
3.  Agregue la extensión creada a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) llamando al método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Cree un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) y llame al método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , especificando la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en la entrada.
5.  Recupere un objeto de colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) llamando a la propiedad [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) en un objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.

## <a name="resetextensions"></a>resetExtensions

La función [**resetExtensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) de Xenroll.dll quita la colección de extensiones de la solicitud.

Para quitar una extensión de una solicitud por número de índice mediante CertEnroll.dll, llame al método [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) en la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) . Para quitar todos los atributos de una solicitud, llame al método [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
