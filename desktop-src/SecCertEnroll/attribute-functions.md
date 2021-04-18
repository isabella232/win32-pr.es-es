---
description: Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una entidad de certificación (CA) información adicional que puede utilizar al crear y emitir un certificado.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Funciones de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276679"
---
# <a name="attribute-functions"></a>Funciones de atributo

Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) información adicional que puede utilizar al crear y emitir un certificado.

CertEnroll.dll implementa las interfaces siguientes para definir atributos y colecciones de atributos:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

En las secciones siguientes se identifican las funciones exportadas por Xenroll.dll para asociar atributos criptográficos con solicitudes de certificado y se describe cómo usar CertEnroll.dll para reemplazar la función o para indicar que no existe ninguna asignación entre las dos bibliotecas:

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [ClientId](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [Temas relacionados](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

La función [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) de Xenroll.dll agrega un atributo a una solicitud de certificado.

En general, para agregar un atributo a una solicitud usando los objetos implementados en CertEnroll.dll, puede realizar las siguientes acciones:

1.  Cree un objeto de colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .
2.  Cree un objeto [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) y llame al método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) para crear un atributo a partir de un identificador de objeto y un valor de atributo, o use cualquiera de las interfaces enumeradas anteriormente para definir uno de los atributos más comunes.
3.  Agregue cada nuevo atributo creado en el paso anterior a la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) mediante el método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .
4.  Cree un objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) e Inicialícelo llamando al método [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) y especificando la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) en la entrada.
5.  Recupere un objeto de colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) llamando a la propiedad [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) en un objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.
6.  Agregue el objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Los atributos autenticados son pares nombre-valor que están firmados por y se agregan a una firma. La función [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) de Xenroll.dll agrega una matriz de atributos autenticados a una solicitud [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .

Como se explicó anteriormente para la función [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , puede utilizar CertEnroll.dll para definir y agregar fácilmente una colección de atributos a una solicitud de certificado. Sin embargo, no puede elegir si el atributo está autenticado. El proceso de inscripción toma esta decisión automáticamente.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

La función [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) de Xenroll.dll agrega un par nombre-valor no autenticado a una solicitud.

Puede usar la interfaz [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) en CertEnroll.dll para definir un par nombre-valor, y puede Agregar una colección de pares nombre-valor a un objeto de solicitud CMC realizando las siguientes acciones:

1.  Cree e inicialice un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . El proceso de inicialización crea una colección [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vacía.
2.  Llame a la propiedad [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) en un objeto de solicitud CMC existente para recuperar la colección.
3.  Cree e inicialice un objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .
4.  Agregue cada nuevo par nombre-valor a la colección [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) llamando al método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .

El proceso de inscripción coloca la colección de pares nombre-valor en la estructura **TaggedAttribute** de la solicitud CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

La función [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) de Xenroll.dll agrega un par nombre-valor autenticado a una solicitud. Normalmente se usa para especificar el nombre del solicitante en una solicitud de inscripción en nombre de (EOBO).

En CertEnroll.dll, use la propiedad [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) para especificar el nombre en una solicitud EOBO.

## <a name="clientid"></a>ClientId

La función [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) de Xenroll.dll especifica o recupera un atributo **ClientID** .

Use la propiedad [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) en CertEnroll.dll para agregar este atributo a una solicitud CMC o PKCS \# 10.

## <a name="renewalcertificate"></a>RenewalCertificate

La función [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) de Xenroll.dll especifica o recupera un atributo **RenewalCertificate** .

En CertEnroll.dll, cuando se llama a [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) en un \# objeto PKCS 7 o PKCS), se crea automáticamente.

## <a name="resetattributes"></a>resetAttributes

La función [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) de Xenroll.dll quita la colección de atributos de una solicitud.

Para quitar un atributo de una solicitud por índice mediante CertEnroll.dll, llame al método [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) en la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) . Para quitar todos los atributos de una solicitud, llame al método [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
