---
description: Crea un objeto de solicitud PKCS \# 7 para renovar un certificado existente. El objeto de solicitud usa un nuevo par de claves, pero conserva el proveedor criptográfico asociado al certificado que se va a renovar.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3da14719cc2a9e6bdf4c16cad57d24b9ee4ec0c2ee955cc8b7c20643b2b6f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740435"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

El ejemplo enrollRenewalPKCS7 crea un objeto de solicitud PKCS \# 7 para renovar un certificado existente. El objeto de solicitud usa un nuevo par de claves, pero conserva el proveedor criptográfico asociado al certificado que se va a renovar.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta vc enrollRenewalPKCS7 de *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollRenewalPKCS7.

## <a name="discussion"></a>Debate

El ejemplo enrollRenewalPKCS7:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla utilizada para crear la solicitud de certificado.
2.  Recupera un certificado existente mediante el nombre de la plantilla especificada en la línea de comandos o, si no se encuentra un certificado, intenta inscribir uno mediante la plantilla. Las funciones findCertByTemplate e enrollCertByTemplate se definen en enrollCommon.cpp.
3.  Comprueba la cadena de certificados y convierte el certificado en **un BSTR**.
4.  Crea un [**objeto IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e inicializa mediante el certificado existente. Dado que *el parámetro inheritOptions* se establece en InheritDefault, se crea un nuevo par de claves para la solicitud, pero se usa el proveedor criptográfico del certificado existente. Para obtener más información, vea el [**método InitializeFromCertificate.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate)
5.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante el objeto de solicitud PKCS 7, intenta inscribirlo con la entidad de certificación y supervisa el estado del proceso \# de inscripción. La función checkEnrollStatus se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Solicitud de renovación pkcs \# 7](pkcs--7--renewal-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



