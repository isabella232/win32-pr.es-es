---
description: Inscribe un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre del sujeto y la longitud, en bits, de la clave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4763e3ae68404e47207dccdb75c759fc30394e849bee07a71f2c54c649347a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669915"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

El ejemplo enrollSimpleUserCert inscribe un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre del sujeto y la longitud, en bits, de la clave.

## <a name="location"></a>Location

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollSimpleUserCert. Se instala una versión de C# en la carpeta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples \\ X509 Certificate Enrollment \\ CSharp \\ EnrollSimpleUserCert .

## <a name="discussion"></a>Debate

El ejemplo enrollSimpleUserCert:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla, el nombre del sujeto y la longitud de la clave.
2.  Crea un [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e inicializa mediante la plantilla .
3.  Recupera el objeto de solicitud de certificado interno del objeto de inscripción y lo consulta para el [**objeto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) La solicitud más interna siempre es una solicitud PKCS \# 10.
4.  Recupera el [**objeto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) de la solicitud PKCS 10 y establece la longitud de clave \# especificada en la línea de comandos.
5.  Crea un [**objeto IX500DistinguishedName,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) lo usa para codificar el nombre del sujeto X.500 y agrega el nombre a la solicitud PKCS \# 10.
6.  Intenta inscribir al usuario final con la entidad de certificación y supervisa el progreso del proceso de inscripción. La función checkEnrollStatus se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



