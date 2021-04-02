---
description: La biblioteca CertEnroll.dll implementa cinco interfaces que se pueden utilizar para crear y administrar una solicitud de certificado.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Funciones de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04191f49949f662a9b9d780726f7ac7a40b370ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082219"
---
# <a name="certificate-request-functions"></a>Funciones de solicitud de certificado

La biblioteca CertEnroll.dll implementa cinco interfaces que se pueden utilizar para crear y administrar una solicitud de certificado. De estos, la interfaz [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) representa un objeto base abstracto que define las firmas de método heredadas por las cuatro interfaces siguientes.

| Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Permite crear un certificado directamente sin aplicarlo a una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA).<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa una solicitud de certificado de [*Administración de certificados sobre CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (mensaje de administración de certificados sobre CMS) que puede contener una solicitud anidada de PKCS \# 10 u otro objeto de solicitud de CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa un objeto de solicitud de sintaxis de mensajes de certificado [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) (CMS) que debe contener una solicitud anidada PKCS \# 10.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa una \# solicitud de certificado PKCS 10. Una \# solicitud PKCS 10 se puede enviar directamente a una entidad de certificación o puede estar incluida en una \# solicitud PKCS 7 o CMC.<br/>                                                                                                                                                            |



 

Puede usar un objeto de solicitud de certificado para inicializar un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para inscribir un cliente en una jerarquía de certificados e instalar la respuesta de certificado devuelta por la CA.

En cada una de las secciones siguientes se identifica una función exportada por Xenroll.dll para crear, enumerar o eliminar solicitudes de certificado. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas:

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

La función [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) de Xenroll.dll crea una solicitud de certificado PKCS 10 codificada en Base64 \# y la guarda en un archivo.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para escribir una solicitud en un archivo. Sin embargo, puede recuperar una solicitud de certificado mediante una llamada a la propiedad [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) del objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) y crear una función personalizada para copiar el valor en un archivo.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

La función [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) de Xenroll.dll crea una \# solicitud de certificado PKCS 7, PKCS \# 10 o CMC y la guarda en un archivo.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para escribir una solicitud en un archivo. Sin embargo, puede recuperar una solicitud de certificado mediante una llamada a la propiedad [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) del objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) y crear una función personalizada para copiar el valor en un archivo.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

La función [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) de Xenroll.dll crea una \# solicitud de certificado PKCS 10 y la copia en una matriz de bytes.

Puede usar un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para inicializar una \# solicitud PKCS 10 a partir de una solicitud existente, un certificado existente, una [*clave privada*](/windows/desktop/SecGloss/p-gly), una [*clave pública*](/windows/desktop/SecGloss/p-gly)o una plantilla.

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

La función [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) de Xenroll.dll crea una \# solicitud de certificado PKCS 7 y la copia en una matriz de bytes.

Puede usar un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para inicializar una \# solicitud PKCS 7 a partir de una solicitud existente, un certificado existente, un objeto de solicitud interno o una plantilla.

## <a name="createrequestwstr"></a>createRequestWStr

La función [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) de Xenroll.dll crea una \# solicitud de certificado PKCS 7, PKCS \# 10 o CMC y la copia en una matriz de bytes.

Para usar la biblioteca de CertEnroll.dll para crear \# solicitudes PKCS 7, PKCS \# 10 o CMC, puede crear e inicializar instancias de los objetos [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

## <a name="deleterequestcert"></a>DeleteRequestCert

La función [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) de Xenroll.dll especifica o recupera un valor booleano que indica si se quita un certificado ficticio después de instalar una respuesta de certificado.

El objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) de CertEnroll.dll crea automáticamente certificados ficticios en el almacén de solicitudes para guardar temporalmente varias propiedades de certificado que se inicializan durante el proceso de inscripción. Después de que una CA emite un certificado, las propiedades se copian en el nuevo certificado y se elimina el certificado ficticio. La biblioteca CertEnroll.dll no permite forzar que un certificado ficticio permanezca después de instalar la respuesta del certificado.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

La función [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) de Xenroll.dll recupera un valor de propiedad especificado para una solicitud pendiente.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

La función [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) de Xenroll.dll quita una solicitud pendiente del almacén de solicitudes.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente.

## <a name="reset"></a>Reset

La función de [**restablecimiento**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) de Xenroll.dll devuelve el control de inscripción de certificados a un estado inicial.

Puede lograr el mismo resultado mediante Certenroll.dll para crear un nuevo objeto de solicitud del tipo requerido.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

La función [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) de Xenroll.dll especifica las propiedades de la solicitud pendiente.

La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para quitar una solicitud de certificado pendiente. Puede llamar a la propiedad [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) del objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar una cadena de configuración, pero solo para un objeto de inscripción activo.

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

 

