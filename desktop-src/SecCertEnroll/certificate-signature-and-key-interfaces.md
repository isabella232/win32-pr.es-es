---
description: Las siguientes interfaces se pueden usar para administrar firmas de certificados y claves públicas y privadas.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma de certificado e interfaces clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911289"
---
# <a name="certificate-signature-and-key-interfaces"></a>Firma de certificado e interfaces clave

Las siguientes interfaces se pueden usar para administrar firmas de certificados y claves públicas y privadas.



| Interfaz                                                      | Descripción                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Representa un certificado de firma que le permite firmar una solicitud de certificado.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Administra una colección de objetos [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Representa una clave privada asimétrica que se puede usar para el cifrado, la firma y el acuerdo de claves. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Representa una clave pública en un par de claves pública y privada.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Representa la información utilizada para firmar una solicitud de certificado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



