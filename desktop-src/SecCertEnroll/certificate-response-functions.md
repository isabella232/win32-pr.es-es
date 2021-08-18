---
description: Implementa la interfaz IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Funciones de respuesta de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902405"
---
# <a name="certificate-response-functions"></a>Funciones de respuesta de certificado

CertEnroll.dll implementa la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para enviar una solicitud de certificado de cliente e instalar la respuesta de una entidad de [*certificación*](/windows/desktop/SecGloss/c-gly) (CA).

El proceso de inscripción puede dar cabida a los tres escenarios siguientes:

<dl> Inscripción fuera de banda

1.  Llame a cualquier método de inicialización implementado por [**el objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Llame al [**método CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) para recuperar la solicitud.
3.  Envíe la solicitud fuera de banda (manualmente o mediante algún otro proceso).
4.  Recibir la respuesta de una entidad de certificación.
5.  Llame al [**método InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

  
Inscripción automática

1.  Llame a cualquier método de inicialización implementado por [**el objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Llame al [**método Enroll.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)

  
Inscripción retrasada

1.  Llame a cualquier método de inicialización implementado por [**el objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Llame al [**método CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) para recuperar la solicitud.
3.  Almacene la solicitud hasta que esté listo para enviarla.
4.  Cuando esté listo para inscribirse, llame al [**método Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) para reinicializar el objeto de inscripción.
5.  Llame al [**método InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) cuando la ca devuelva un certificado.

  
</dl>

Durante el proceso de inscripción, puede llamar a la propiedad [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) en el objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar un valor de enumeración [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) que identifique si la inscripción se ha producido correctamente, está pendiente, se omitió, generó un error o se denegó.

Cada una de las secciones siguientes identifica una función exportada por Xenroll.dll instalar una respuesta de certificado desde una entidad de certificación. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o indica que no existe ninguna asignación entre las dos bibliotecas:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertContextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertContextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDs](#writecerttouserds)
-   [Temas relacionados](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

La [**función acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) de Xenroll.dll instala una respuesta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) desde un archivo.

La CertEnroll.dll no implementa directamente la funcionalidad para instalar una respuesta de certificado PKCS \# 7 desde un archivo. Sin embargo, puede crear una función personalizada para leer los datos del archivo en una matriz de bytes y llamar a [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar la respuesta.

Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar un certificado sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

La [**función acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) de Xenroll.dll instala una respuesta de certificado PKCS \# 7 o CMC desde un archivo.

La CertEnroll.dll no implementa directamente la funcionalidad para instalar una respuesta de certificado desde un archivo. Sin embargo, puede crear una función personalizada para leer los datos del archivo en una matriz de bytes y llamar a [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar la respuesta PKCS \# 7 o CMC.

Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar un certificado sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

La [**función acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) de Xenroll.dll instala una respuesta PKCS \# 7 contenida en una matriz de bytes.

Puede llamar a [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar un mensaje PKCS \# 7. Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar la respuesta PKCS 7 sin llamar primero a Enroll o \# [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="acceptresponseblob"></a>acceptResponseBlob

La [**función acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) de Xenroll.dll instala una respuesta de certificado PKCS \# 7 o CMC contenida en una matriz de bytes.

Puede llamar a [**InstallResponse para**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) instalar una respuesta PKCS \# 7 o CMC. Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar la respuesta sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

La [**función getCertContextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) de Xenroll.dll recupera el certificado de cliente de un archivo.

La CertEnroll.dll no implementa directamente la funcionalidad para recuperar un certificado de una respuesta de ca guardada en un archivo. Sin embargo, puede crear una función personalizada para leer los datos del archivo en una matriz de bytes y llamar a [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar la respuesta PKCS 7 o CMC y llamar a la propiedad Certificate para recuperar el \# certificado. [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate)

Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar un certificado sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

La [**función getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) de Xenroll.dll recupera el certificado de cliente de una respuesta PKCS \# 7.

Puede llamar a la [**propiedad Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) en el [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar un certificado después de llamar al método [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

La [**función getCertContextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) de Xenroll.dll recupera un certificado de cliente de una respuesta PKCS \# 7 o CMC.

Puede llamar a la [**propiedad Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) en el [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar un certificado después de llamar al método [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

La [**función InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) de Xenroll.dll instala una respuesta PKCS \# 7.

Puede llamar a [**InstallResponse para**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) instalar una respuesta PKCS \# 7 o CMC. Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar la respuesta sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

La [**función InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) de Xenroll.dll instala una respuesta PKCS 7 y devuelve el número de \# certificados instalados.

Puede llamar a [**InstallResponse para**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) instalar una respuesta PKCS \# 7 o CMC. Si especifica el valor **AllowNoOutstandingRequest** de la enumeración [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para el primer parámetro de [**InstallResponse,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)no es necesario que exista un certificado ficticio, lo que le permite instalar la respuesta sin llamar primero a [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) Sin embargo, si va a instalar un certificado mediante un script web, debe existir un certificado ficticio en el almacén de solicitudes. Por lo tanto, **debe especificar AllowNone** para el primer parámetro.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

La [**función SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) de Xenroll.dll especifica o recupera el nombre del archivo en el que se va a guardar la respuesta del certificado. La CertEnroll.dll no implementa la funcionalidad que le permite copiar un certificado en un archivo específico. El proceso de inscripción instala automáticamente la cadena de certificados en los archivos de los almacenes adecuados.

## <a name="writecerttocsp"></a>WriteCertToCSP

La [**función WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) de Xenroll.dll especifica o recupera un valor booleano que indica si un certificado debe escribirse en un proveedor de servicios criptográficos [*(CSP).*](/windows/desktop/SecGloss/c-gly) Normalmente, si se llama a esta función, el proveedor es una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly).

En CertEnroll.dll, cuando un cliente llama al método [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para enviar una solicitud de un certificado de tarjeta inteligente y se emite un certificado, [**Inscribir**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) instala automáticamente el certificado en la tarjeta inteligente, suponiendo que la tarjeta esté instalada en el lector. El [**método InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) también escribe automáticamente el certificado en la tarjeta inteligente.

## <a name="writecerttouserds"></a>WriteCertToUserDs

La [**función WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) de Xenroll.dll especifica o recupera un valor booleano que indica si se debe guardar un certificado en el almacén Active Directory datos. La CertEnroll.dll no implementa la funcionalidad que le permite especificar un almacén en el que copiar un certificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
