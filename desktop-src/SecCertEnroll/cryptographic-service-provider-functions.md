---
description: Funciones exportadas por Xenroll.dll que se pueden utilizar para administrar un proveedor de servicios criptográficos.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Funciones de proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a981b418271ba834352c0301c005b39742729a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808666"
---
# <a name="cryptographic-service-provider-functions"></a>Funciones de proveedor de servicios criptográficos

En cada una de las secciones siguientes se identifica una función exportada por Xenroll.dll que se puede usar para administrar un proveedor de servicios criptográficos. En cada tema también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas:

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Temas relacionados](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

La función [**EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) de Xenroll.dll recupera una colección de algoritmos criptográficos.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar información acerca de los algoritmos admitidos por un [*proveedor de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP):

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado del paso 4.
6.  Llame a la propiedad [**CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) en un objeto [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) específico en la colección [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) recuperada en el paso 5.

## <a name="enumcontainerswstr"></a>enumContainersWStr

La función [**enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) de Xenroll.dll recupera un contenedor de claves de la colección por índice.

La biblioteca CertEnroll.dll no implementa directamente esta funcionalidad.

## <a name="enumproviderswstr"></a>enumProvidersWStr

La función [**enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) de Xenroll.dll recupera un proveedor de servicios de cifrado de la colección por índice.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar la colección de contenedores criptográficos:

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado del paso 4.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

La función [**GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) de Xenroll.dll recupera el nombre de un [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly).

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el nombre del algoritmo:

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para recuperar el identificador de objeto del algoritmo.
6.  Llame a la propiedad [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) de la interfaz [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) para recuperar el nombre para mostrar del algoritmo.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

La función [**getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) de Xenroll.dll recupera el tipo de proveedor de servicios criptográficos.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el tipo de proveedor:

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado en el paso 4.

## <a name="hashalgid"></a>HashAlgID

La función [**HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) de Xenroll.dll recupera un valor entero que contiene el identificador del algoritmo utilizado para firmar una solicitud.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el algoritmo hash:

-   Recupere una interfaz [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) llamando a la propiedad [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) en una \# solicitud PKCS 10 o CMC o la propiedad [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) en una solicitud [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .
-   Llame a la propiedad [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) en el objeto de información de firma para recuperar el identificador de objeto del algoritmo hash.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

La función [**HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) de Xenroll.dll especifica o recupera un valor de cadena que identifica el algoritmo hash utilizado para firmar una solicitud.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el algoritmo hash:

-   Recupere una interfaz [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) llamando a la propiedad [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) en una \# solicitud PKCS 10 o CMC o la propiedad [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) en una \# solicitud PKCS 7.
-   Llame a la propiedad [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) en el objeto de información de firma para recuperar el identificador de objeto del algoritmo hash.
-   Llame a la propiedad [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) de la interfaz [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) devuelta en el paso 2 para recuperar el nombre para mostrar del algoritmo.

## <a name="providerflags"></a>ProviderFlags

La función [**ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) de Xenroll.dll especifica o recupera las marcas usadas al adquirir un identificador a un CSP.

La biblioteca CertEnroll.dll no asigna esta función perfectamente, pero puede obtener información de propiedad enriquecida del objeto de inscripción y la [*clave privada*](/windows/desktop/SecGloss/p-gly). Para obtener más información, examine las propiedades expuestas por las interfaces [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .

## <a name="providernamewstr"></a>ProviderNameWStr

La función [**ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) de Xenroll.dll especifica o recupera el nombre de un CSP.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el nombre del proveedor:

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**providerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado en el paso 4.

## <a name="providertype"></a>ProviderType

La función [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) de Xenroll.dll especifica o recupera un valor entero que identifica el tipo del CSP.

Al usar CertEnroll.dll, puede realizar las siguientes acciones para recuperar el tipo de proveedor:

1.  Llame a la propiedad de [**solicitud**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) en un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Llame al método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) en la solicitud que ha devuelto el paso 1 para recuperar la solicitud más interna.
3.  Llame a **QueryInterface** en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) que ha devuelto el paso 2 para convertirlo en un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Llame a la propiedad [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) en la \# solicitud PKCS 10.
5.  Llame a la propiedad [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) en el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado en el paso 4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
