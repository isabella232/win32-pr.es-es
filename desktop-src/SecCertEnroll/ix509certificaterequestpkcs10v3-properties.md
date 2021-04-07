---
description: La interfaz IX509CertificateRequestPkcs10V3 expone las siguientes propiedades.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Propiedades de IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002968"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Propiedades de IX509CertificateRequestPkcs10V3

La interfaz [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Certificado que se usa para cifrar los valores de EKPUB y EKCERT desde el cliente. Esta propiedad debe establecerse en un certificado válido que se encadena a una raíz de equipo de confianza.<br/>                                                                                                                                                                                |
| [**Propiedad AttestPrivateKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True si se debe atestar la clave privada creada; en caso contrario, false. Si es true, se espera que se haya establecido la propiedad [**AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) . <br/>                                                                                                        |
| [**Propiedad ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | La contraseña que se va a usar al crear una solicitud con un desafío. Para crear una solicitud sin un desafío, no establezca la propiedad [**ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) .<br/>                                                                                                                                      |
| [**Propiedad EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Algoritmo de cifrado que se usa para cifrar los valores de EKPUB y EKCERT desde el cliente.<br/>                                                                                                                                                                                                                                                               |
| [**Propiedad EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifica la longitud de bits para el [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) que se va a usar para el cifrado. Si el **EncryptionAlgorithm** solo admite una longitud de bit, no es necesario especificar un valor para la propiedad [**EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) .<br/> |
| [**Propiedad NameValuePairs**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Colección de pares de nombre/valor de valores de propiedad de certificado adicionales.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




