---
description: La interfaz IX509CertificateRequestPkcs10V3 expone las siguientes propiedades.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Propiedades IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcc126c21ca5fee5e8d1c15dd2561439c7a35f0f6cef637177ff36160a22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976225"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Propiedades IX509CertificateRequestPkcs10V3

La [**interfaz IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttestationEncryptionCertificate, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Certificado que se usa para cifrar los valores EKPUB y EKCERT del cliente. Esta propiedad debe establecerse en un certificado válido que se encadena a una raíz de máquina de confianza.<br/>                                                                                                                                                                                |
| [**Propiedad AttestPrivateKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True si es necesario atestiguar la clave privada creada; en caso contrario, false. Si es true, se espera que se haya establecido la propiedad [**AttestationEncryptionCertificate.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) <br/>                                                                                                        |
| [**ChallengePassword, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Contraseña que se usará al crear una solicitud con un desafío. Para crear una solicitud sin un desafío, no establezca la [**propiedad ChallengePassword.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                                                                                                                                      |
| [**EncryptionAlgorithm, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Algoritmo de cifrado utilizado para cifrar los valores EKPUB y EKCERT del cliente.<br/>                                                                                                                                                                                                                                                               |
| [**EncryptionStrength, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifica la longitud de bits de [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) que se usará para el cifrado. Si **EncryptionAlgorithm** solo admite una longitud de un bit, no es necesario especificar un valor para la [**propiedad EncryptionStrength.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/> |
| [**NameValuePairs, propiedad**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Colección de pares nombre-valor de valores de propiedad de certificado adicionales.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




