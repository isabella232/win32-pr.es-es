---
description: Crea una solicitud PKCS 7 a partir de un certificado existente mediante la herencia de las claves públicas \# y privadas y la plantilla de certificado.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0635fdf4daacc9c7a04db98c7e34e9d3495c6f18ca3e145b166f19e3cd49610a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779956"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

El ejemplo enrollPKCS7 crea una solicitud PKCS 7 a partir de un certificado existente mediante la herencia de las claves públicas y privadas \# y la plantilla de certificado. El certificado existente se usa para firmar la solicitud. En este ejemplo se inscribe al usuario en una jerarquía de certificados y se instala la respuesta del certificado. En el ejemplo se usa un certificado existente para inscribir e instalar uno nuevo. Para obtener más información sobre cómo renovar un certificado existente, [vea enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta vc enrollPKCS7 *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollPKCS7.

## <a name="discussion"></a>Debate

El ejemplo enrollPKCS7:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla de certificado usada para buscar un certificado existente.
2.  Recupera un certificado existente mediante el nombre de la plantilla especificada en la línea de comandos o, si no se encuentra un certificado, intenta inscribir uno nuevo creado mediante la plantilla. Las funciones findCertByTemplate e enrollCertByTemplate se definen en enrollCommon.cpp.
3.  Comprueba la cadena de certificados y convierte el certificado en **un BSTR**.
4.  Crea un [**objeto IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e inicializa mediante el certificado existente. El nuevo objeto de solicitud PKCS 7 hereda las claves privadas y públicas y la \# plantilla del certificado existente.
5.  Crea un [**objeto ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inicializa mediante el certificado existente y lo agrega al objeto de solicitud PKCS \# 7.
6.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante el objeto de solicitud PKCS 7, intenta inscribirlo con la entidad de certificación y supervisa el estado del proceso \# de inscripción. La función checkEnrollStatus se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



