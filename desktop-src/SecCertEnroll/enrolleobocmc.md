---
description: Crea una solicitud de certificado CMC en nombre de otro usuario e inscribe el usuario en una jerarquía de certificados.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542683"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

El ejemplo enrollEOBOCMC crea una solicitud de certificado CMC en nombre de otro usuario e inscribe el usuario en una jerarquía de certificados. La inscripción en nombre de otro usuario requiere que la solicitud de certificado se firme con un certificado de agente de inscripción.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollEOBOCMC

## <a name="discussion"></a>Debate

El ejemplo enrollEOBOCMC:

1.  Procesa los siguientes argumentos de la línea de comandos:
    -   Nombre de una plantilla de certificado.
    -   Nombre del usuario que solicita el certificado.
    -   El nombre de un archivo de intercambio de información personal (PFX) en el que se guardará la solicitud.
    -   Contraseña que se va a usar con el archivo PFX.
    -   Un nombre de plantilla de agente de inscripción opcional. La plantilla se usa para crear un certificado de agente de inscripción si no existe ninguno en el almacén de certificados.
2.  Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el uso de la plantilla de certificado especificada en la línea de comandos.
3.  Agrega el nombre del solicitante al objeto de solicitud de CMC.
4.  Recupera un certificado de agente de inscripción existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla de agente de inscripción especificada en la línea de comandos e intenta inscribirla.
5.  Comprueba la cadena de certificados que contiene el certificado de agente de inscripción.
6.  Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de agente de inscripción, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud CMC y agrega el objeto de certificado de firma del agente de inscripción a la colección. El objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) que se describe en el siguiente paso usa el certificado para firmar la solicitud CMC.
7.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante la solicitud CMC, intenta inscribirse y comprueba el progreso del proceso de inscripción.
8.  Exporta el certificado instalado a un archivo PFX. El archivo está protegido mediante la contraseña especificada en la línea de comandos. La función EncodeToFileW se define en enrollCommon. cpp.
9.  Elimina el certificado del almacén de certificados. Las funciones que se usan en el siguiente ejemplo de código se pueden encontrar en la documentación de CryptoAPI.
10. Elimina la clave privada del equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud EOBO de CMC](cmc-eobo-request.md)
</dt> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



