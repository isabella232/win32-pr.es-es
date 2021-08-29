---
description: Crea una solicitud de certificado de CMC en nombre de otro usuario e inscribe al usuario en una jerarquía de certificados.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a9dbcddf5495f5a58d161e5bf086c737691b52312827d3420ca13a47440822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882995"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

El ejemplo enrollEOBOCMC crea una solicitud de certificado de CMC en nombre de otro usuario e inscribe al usuario en una jerarquía de certificados. La inscripción en nombre de otro usuario requiere que la solicitud de certificado se firme mediante un certificado de agente de inscripción.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *%ProgramFiles%* \\ microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollEOBOCMC .

## <a name="discussion"></a>Debate

El ejemplo enrollEOBOCMC:

1.  Procesa los siguientes argumentos de línea de comandos:
    -   Nombre de una plantilla de certificado.
    -   Nombre del usuario que solicita el certificado.
    -   Nombre de un archivo de Exchange personal (PFX) en el que se va a guardar la solicitud.
    -   Contraseña que se usará con el archivo PFX.
    -   Un nombre de plantilla de agente de inscripción opcional. La plantilla se usa para crear un certificado de agente de inscripción si no existe ninguno en el almacén de certificados.
2.  Crea un [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante la plantilla de certificado especificada en la línea de comandos.
3.  Agrega el nombre del solicitante al objeto de solicitud de CMC.
4.  Recupera un certificado de agente de inscripción existente o, si no se encuentra uno, crea una solicitud de certificado a partir de la plantilla del agente de inscripción especificada en la línea de comandos e intenta inscribirla.
5.  Comprueba la cadena de certificados que contiene el certificado del agente de inscripción.
6.  Crea un objeto [**ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inicializa mediante el certificado del agente de inscripción, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud de CMC y agrega el objeto de certificado de firma del agente de inscripción a la colección. El [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) que se describe en el paso siguiente usa el certificado para firmar la solicitud de CMC.
7.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante la solicitud de CMC, intenta inscribirlo y comprueba el progreso del proceso de inscripción.
8.  Exporta el certificado instalado a un archivo PFX. El archivo está protegido mediante la contraseña especificada en la línea de comandos. La función EncodeToFileW se define en enrollCommon.cpp.
9.  Elimina el certificado del almacén de certificados. Las funciones usadas en el ejemplo de código siguiente se pueden encontrar en la documentación de CryptoAPI.
10. Elimina la clave privada del equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud EOBO de CMC](cmc-eobo-request.md)
</dt> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



