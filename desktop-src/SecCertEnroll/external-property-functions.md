---
description: Las propiedades se usan para asociar un valor a un certificado.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Funciones de propiedad externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c8148022bf604aa90780787c068b330c469ae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069029"
---
# <a name="external-property-functions"></a>Funciones de propiedad externa

Las propiedades se usan para asociar un valor a un certificado. Las propiedades nunca se envían ni procesan por una entidad [*de certificación*](/windows/desktop/SecGloss/c-gly) (CA) y no se almacenan dentro de un certificado. Normalmente, se asocian a un certificado después de recibir el certificado de la entidad de certificación y antes de guardarlo en un almacén. Las propiedades se guardan en el almacén junto con el certificado. CertEnroll.dll implementa la [**interfaz ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) y las siguientes interfaces derivadas de **ICertProperty**:

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

Cada una de las secciones siguientes identifica una función exportada por Xenroll.dll administrar propiedades de certificado externo. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o indica que no existe ninguna asignación entre las dos bibliotecas:

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [ThumbPrintWStr](#thumbprintwstr)
-   [Temas relacionados](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

La [**función addBlobPropertyToCertificateWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) de Xenroll.dll agrega una propiedad al certificado.

En CertEnroll.dll, todos los objetos derivados de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementan un [**método SetValueOnCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) que puede usar para asociar una propiedad a un certificado. Además, el [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementa directamente las propiedades [**CertificateFriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) [**y CertificateDescription.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription)

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

La [**función GetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) de Xenroll.dll recupera el certificado de exchange usado para archivar una [*clave privada.*](/windows/desktop/SecGloss/p-gly)

Puede usar el [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) en CertEnroll.dll para crear una solicitud para que una entidad de certificación archive la clave privada. Debe recuperar un certificado de intercambio [](/windows/desktop/SecGloss/p-gly) de la entidad de certificación y usar la clave pública contenida en ese certificado para cifrar la clave privada que va a enviar para su archivado. Para especificar o recuperar un certificado de intercambio de CA, llame a la [**propiedad KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) en ese objeto.

## <a name="resetblobproperties"></a>resetBlobProperties

La [**función resetBlobProperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) de Xenroll.dll quita la colección de propiedades del certificado.

En CertEnroll.dll, todos los objetos de propiedad derivados de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementan la [**propiedad RemoveFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) que puede usar para desasociar una propiedad de un certificado.

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

La [**función SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) de Xenroll.dll especifica un certificado de exchange que se usa para archivar una clave privada.

Puede usar el [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) en CertEnroll.dll para crear una solicitud para que una entidad de certificación archive la clave privada. Debe recuperar un certificado de intercambio de la entidad de certificación y usar la clave pública contenida en ese certificado para cifrar la clave privada que va a enviar para su archivado. Para especificar o recuperar un certificado de intercambio de CA, llame a la [**propiedad KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) en ese objeto.

## <a name="setsignercertificate"></a>SetSignerCertificate

La [**función SetSignerCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) de Xenroll.dll especifica un certificado de firmante.

El [**objeto ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) de CertEnroll.dll se puede usar para firmar una solicitud de certificado [*PKCS \# 7,*](/windows/desktop/SecGloss/p-gly)CMC o [*autofirmado.*](/windows/desktop/SecGloss/c-gly) Puede inicializar el objeto mediante un certificado de firma existente y asociarlo a una solicitud llamando a una de las propiedades siguientes:

-   [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) en [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) en [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) en [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Además, si inicializa una solicitud de CMC desde una solicitud interna y una plantilla o inicializa una solicitud PKCS 7 desde una solicitud existente, se puede establecer el certificado \# de firma.

## <a name="thumbprintwstr"></a>ThumbPrintWStr

La [**función ThumbPrintWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) Xenroll.dll especifica o recupera el valor del hash del certificado.

En CertEnroll.dll, puede usar el objeto [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) para recuperar un [*valor hash*](/windows/desktop/SecGloss/h-gly) [*(huella*](/windows/desktop/SecGloss/t-gly)digital) creado mediante una llamada al [**método InitializeFromCertificate.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
