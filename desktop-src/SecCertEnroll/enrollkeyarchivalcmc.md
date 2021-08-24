---
description: Crea una solicitud de certificado de CMC para archivar una clave privada en una entidad de certificación (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e2e9856309560e982e7e1dda7ba724fefd0759e6fa10196b321eb66947cf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882955"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

El ejemplo enrollKeyArchivalCMC crea una solicitud de certificado de CMC para archivar una clave privada en una entidad de certificación (CA). Para obtener más información, vea [Solicitud de archivo de clave DE CMC.](cmc-key-archival-request.md)

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta enrollKeyArchivalCMC de *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollKeyArchivalCMC.

## <a name="discussion"></a>Debate

El ejemplo enrollKeyArchivalCMC:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla de certificado que se usará para la inscripción.
2.  Crea un objeto de solicitud de certificado [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa para un contexto de usuario final mediante el nombre de plantilla.
3.  Establece la [**propiedad ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) en la solicitud de CMC.
4.  Crea un [**objeto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de ca.
5.  Crea un objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) y lo usa para recuperar el certificado de intercambio para la CA.
6.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante la solicitud CMC, crea una cadena codificada en Base64 que contiene la solicitud de archivo de clave y la envía a la entidad de certificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de archivo de clave de CMC](cmc-key-archival-request.md)
</dt> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
