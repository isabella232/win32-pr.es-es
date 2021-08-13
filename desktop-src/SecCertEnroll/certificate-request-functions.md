---
description: La CertEnroll.dll implementa cinco interfaces que se pueden usar para crear y administrar una solicitud de certificado.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Funciones de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902574"
---
# <a name="certificate-request-functions"></a>Funciones de solicitud de certificado

La CertEnroll.dll implementa cinco interfaces que se pueden usar para crear y administrar una solicitud de certificado. De estas, la [**interfaz IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) representa un objeto base abstracto que define las firmas de método heredadas por las cuatro interfaces siguientes.

| Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Permite crear un certificado directamente sin aplicarlo a una entidad [*de certificación*](/windows/desktop/SecGloss/c-gly) (CA).<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa una solicitud de certificado de Administración de certificados a través de [*CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (Mensaje de administración de certificados sobre CMS) que puede contener una solicitud PKCS 10 anidada u otro objeto de solicitud \# de CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa un objeto de solicitud de sintaxis de mensajes de certificado [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) (CMS) que debe contener una solicitud PKCS \# 10 anidada.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa una solicitud de certificado PKCS \# 10. Una solicitud PKCS 10 se puede enviar directamente a una entidad de certificación o se puede encapsular mediante una \# solicitud PKCS \# 7 o CMC.<br/>                                                                                                                                                            |



 

Puede usar un objeto de solicitud de certificado para inicializar un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para inscribir un cliente en una jerarquía de certificados e instalar la respuesta de certificado devuelta por la CA.

Cada una de las secciones siguientes identifica una función exportada por Xenroll.dll crear, enumerar o eliminar solicitudes de certificado. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o indica que no existe ninguna asignación entre las dos bibliotecas:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [Reset](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [Temas relacionados](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

La [**función createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) de Xenroll.dll crea una solicitud de certificado PKCS 10 codificada en base64 y la guarda en \# un archivo.

La CertEnroll.dll no implementa directamente la funcionalidad para escribir una solicitud en un archivo. Sin embargo, puede recuperar una solicitud de certificado llamando a la propiedad [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) y creando una función personalizada para copiar el valor en un archivo.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

La [**función createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) de Xenroll.dll crea una solicitud de certificado PKCS \# 7, PKCS 10 o CMC y la guarda \# en un archivo.

La CertEnroll.dll no implementa directamente la funcionalidad para escribir una solicitud en un archivo. Sin embargo, puede recuperar una solicitud de certificado llamando a la propiedad [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) en el objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) y creando una función personalizada para copiar el valor en un archivo.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

La [**función createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) de Xenroll.dll crea una solicitud de certificado PKCS \# 10 y la copia en una matriz de bytes.

Puede usar un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para inicializar una solicitud PKCS 10 desde una solicitud existente, un certificado existente, una clave privada, una clave pública o una \# plantilla. [](/windows/desktop/SecGloss/p-gly) [](/windows/desktop/SecGloss/p-gly)

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

La [**función CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) de Xenroll.dll crea una solicitud de certificado PKCS 7 y \# la copia en una matriz de bytes.

Puede usar un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para inicializar una solicitud PKCS 7 desde una solicitud existente, un certificado existente, un objeto de solicitud interno o \# una plantilla.

## <a name="createrequestwstr"></a>createRequestWStr

La [**función createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) de Xenroll.dll crea una solicitud de certificado PKCS \# 7, PKCS 10 o CMC y la copia en una \# matriz de bytes.

Para usar la biblioteca CertEnroll.dll para crear solicitudes PKCS 7, PKCS 10 o CMC, puede crear e inicializar instancias de los objetos \# \# [**IX509CertificateRequestPkcs7,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)o [**IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)

## <a name="deleterequestcert"></a>DeleteRequestCert

La [**función DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) de Xenroll.dll especifica o recupera un valor booleano que indica si se quita un certificado ficticio después de instalar una respuesta de certificado.

El [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) de CertEnroll.dll crea automáticamente certificados ficticios en el almacén de solicitudes para guardar temporalmente varias propiedades de certificado que se inicializan durante el proceso de inscripción. Una vez que una entidad de certificación emite un certificado, las propiedades se copian en el nuevo certificado y se elimina el certificado ficticio. La CertEnroll.dll de certificados no permite forzar que un certificado ficticio permanezca una vez instalada la respuesta del certificado.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

La [**función enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) de Xenroll.dll recupera un valor de propiedad especificado para una solicitud pendiente.

La CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

La [**función removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) de Xenroll.dll quita una solicitud pendiente del almacén de solicitudes.

La CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente.

## <a name="reset"></a>Reset

La [**función Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) de Xenroll.dll devuelve el control de inscripción de certificados a un estado inicial.

Puede lograr el mismo resultado mediante el uso de Certenroll.dll para crear un nuevo objeto de solicitud del tipo necesario.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

La [**función setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) de Xenroll.dll especifica las propiedades de la solicitud pendiente.

La CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente. Puede llamar a la [**propiedad CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) en el objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar una cadena de configuración, pero solo para un objeto de inscripción activo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

