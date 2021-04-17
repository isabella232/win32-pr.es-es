---
description: El SDK de inscripción de certificados se puede usar para crear \# solicitudes de certificados PKCS 10, PKCS \# 7, CMC y autofirmado.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Solicitudes de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686994"
---
# <a name="certificate-requests"></a>Solicitudes de certificado

El SDK de inscripción de certificados se puede usar para crear \# solicitudes de certificados PKCS 10, PKCS \# 7, CMC y autofirmado. Cada tipo de solicitud se representa mediante una de las interfaces enumeradas en la tabla siguiente. Todas las interfaces de solicitud heredan directa o indirectamente de la interfaz [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) . 

| Interfaz                                                                        | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa una \# solicitud PKCS 10. Esta interfaz hereda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa una \# solicitud PKCS 7. Esta interfaz hereda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Representa un certificado autofirmado. Esta interfaz hereda de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa una solicitud de CMC. Esta interfaz hereda de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

En la ilustración siguiente se muestra la estructura de herencia de los objetos de solicitud admitidos por la API de inscripción de certificados. Un objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) actúa, directa o indirectamente, como la clase base para todos los objetos de solicitud disponibles.

![estructura de herencia para las interfaces de solicitud](images/certificate-request-inheritance.png)

Independientemente del tipo, una solicitud de certificado contiene información sobre el sujeto que realiza la solicitud, la clave pública del sujeto, un conjunto de atributos, un conjunto de extensiones X. 509 versión 3 (que pueden enviarse como parte de los atributos) y una firma. Estos problemas se abordan en los temas siguientes:

-   [Nombres de sujeto](subject-names.md)
-   [Atributos](attributes.md)
-   [Extensiones](extensions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



