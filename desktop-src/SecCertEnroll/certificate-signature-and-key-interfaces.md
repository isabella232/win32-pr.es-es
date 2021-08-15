---
description: Las interfaces siguientes se pueden usar para administrar firmas de certificado y claves públicas y privadas.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma de certificado e interfaces de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902311"
---
# <a name="certificate-signature-and-key-interfaces"></a>Firma de certificado e interfaces de clave

Las interfaces siguientes se pueden usar para administrar firmas de certificado y claves públicas y privadas.



| Interfaz                                                      | Descripción                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Representa un certificado de firma que le permite firmar una solicitud de certificado.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Administra una colección de [**objetos ISignerCertificate.**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Representa una clave privada asimétrica que se puede usar para el cifrado, la firma y el contrato de clave. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Representa una clave pública en un par de claves pública y privada.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Representa la información utilizada para firmar una solicitud de certificado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



