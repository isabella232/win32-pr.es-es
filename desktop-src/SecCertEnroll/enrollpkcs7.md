---
description: Crea una \# solicitud PKCS 7 desde un certificado existente heredando las claves públicas y privadas y la plantilla de certificado.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808665"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

El ejemplo enrollPKCS7 crea una \# solicitud PKCS 7 a partir de un certificado existente heredando las claves públicas y privadas y la plantilla de certificado. El certificado existente se usa para firmar la solicitud. En este ejemplo se inscribe el usuario en una jerarquía de certificados y se instala la respuesta del certificado. En el ejemplo se utiliza un certificado existente para inscribir e instalar uno nuevo. Para obtener más información sobre cómo renovar un certificado existente, vea [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollPKCS7

## <a name="discussion"></a>Debate

El ejemplo enrollPKCS7:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla de certificado que se usa para buscar un certificado existente.
2.  Recupera un certificado existente usando el nombre de la plantilla especificada en la línea de comandos o, si no se encuentra un certificado, intenta inscribir uno nuevo creado con la plantilla. Las funciones findCertByTemplate y enrollCertByTemplate se definen en enrollCommon. cpp.
3.  Comprueba la cadena de certificados y convierte el certificado en un **BSTR**.
4.  Crea un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) y lo inicializa mediante el certificado existente. El nuevo \# objeto de solicitud PKCS 7 hereda las claves públicas y privadas y la plantilla del certificado existente.
5.  Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado existente y lo agrega al \# objeto de solicitud PKCS 7.
6.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el \# objeto de solicitud PKCS 7, intenta inscribirlo con la CA y supervisa el estado del proceso de inscripción. La función checkEnrollStatus se define en enrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



