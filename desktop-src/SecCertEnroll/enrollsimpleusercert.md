---
description: Inscribe a un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre de sujeto y la longitud, en bits, de la clave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082876"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

El ejemplo enrollSimpleUserCert inscribe a un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre de sujeto y la longitud, en bits, de la clave.

## <a name="location"></a>Location

Cuando se instala el kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollSimpleUserCert Una versión de C# se instala en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Enrollment \\ CSharp \\ EnrollSimpleUserCert

## <a name="discussion"></a>Debate

El ejemplo enrollSimpleUserCert:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de la plantilla, el nombre del firmante y la longitud de la clave.
2.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo inicializa mediante la plantilla.
3.  Recupera el objeto de solicitud de certificado interno del objeto de inscripción y lo consulta para el objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . La solicitud más interna es siempre una \# solicitud PKCS 10.
4.  Recupera el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) de la solicitud PKCS \# 10 y establece la longitud de clave especificada en la línea de comandos.
5.  Crea un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , lo usa para codificar el nombre de sujeto X. 500 y agrega el nombre a la \# solicitud PKCS 10.
6.  Intenta inscribir el usuario final con la CA y supervisa el progreso del proceso de inscripción. La función checkEnrollStatus se define en enrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 



