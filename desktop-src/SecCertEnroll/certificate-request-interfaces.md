---
description: Las interfaces siguientes se pueden usar para crear solicitudes de certificado.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfaces de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba4f16c6aba1be724fcf2639dd64d7988e40b79a5b29a2d500beb3ae66f4ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902564"
---
# <a name="certificate-request-interfaces"></a>Interfaces de solicitud de certificado

Las interfaces siguientes se pueden usar para crear solicitudes de certificado.



| Interfaz                                                                          | Descripción                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Representa la interfaz abstracta de nivel superior para una solicitud de certificado.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Permite crear certificados directamente sin pasar por un registro o una entidad de certificación.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Extiende la interfaz [**IX509CertificateRequestCertificate para**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) habilitar la inicialización desde una plantilla.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Representa una solicitud de CMC.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Extiende la interfaz [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para habilitar la inicialización desde una plantilla.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Representa una solicitud PKCS \# 10.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Extiende la interfaz [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para habilitar la inicialización desde una plantilla.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Extiende la interfaz [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y agrega propiedades que habilitan la atestación de certificados de TPM. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Representa una solicitud PKCS \# 7.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Extiende la interfaz [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para habilitar la inicialización desde una plantilla.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



