---
description: Crea una solicitud de certificado CMC para archivar una clave privada en una entidad de certificación (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686988"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

El ejemplo enrollKeyArchivalCMC crea una solicitud de certificado CMC para archivar una clave privada en una entidad de certificación (CA). Para obtener más información, consulte [solicitud de archivo de clave CMC](cmc-key-archival-request.md).

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollKeyArchivalCMC

## <a name="discussion"></a>Debate

El ejemplo enrollKeyArchivalCMC:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla de certificado que se va a usar para la inscripción.
2.  Crea un objeto de solicitud de certificado [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa para un contexto de usuario final mediante el nombre de la plantilla.
3.  Establece la propiedad [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) en la solicitud CMC.
4.  Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
5.  Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa para recuperar el certificado de Exchange para la CA.
6.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante la solicitud CMC, crea una cadena codificada en Base64 que contiene la solicitud de archivo de clave y la envía a la CA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de archivo de clave de CMC](cmc-key-archival-request.md)
</dt> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
