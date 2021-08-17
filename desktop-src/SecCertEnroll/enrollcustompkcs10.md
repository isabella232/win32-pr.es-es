---
description: Crea una solicitud PKCS 10 personalizada, la envía a una entidad de certificación independiente (CA) e instala el certificado emitido en el \# almacén de certificados.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b1e955ecd369794e832f16afff1594ed1df1271494d7172832132d4cb7863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780034"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

El ejemplo enrollCustomPKCS10 crea una solicitud PKCS 10 personalizada, la envía a una entidad de certificación independiente (CA) e instala el certificado emitido en el almacén de \# certificados. Una CA independiente no requiere Active Directory y no usa plantillas.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta vc enrollCustomPKCS10 de *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10.

## <a name="discussion"></a>Debate

El ejemplo enrollCustomPKCS10:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre del sujeto del certificado X.500, el nombre del correo electrónico (RFC822) y un identificador de objeto (OID) uso mejorado de clave (EKU). Por ejemplo, puede especificar los argumentos siguientes para inscribir *user1@example.com* :
    -   Nombre del sujeto: "*CN=user1,DC=example,DC=com*"
    -   Nombre RFC822: *user1@example.com*
    -   OID de EKU de autenticación de cliente: 1.3.6.1.5.5.7.3.2
2.  Crea un [**objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa para el usuario final especificando el valor **ContextUser** de la enumeración [**X509CertificateEnrollmentContext.**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext)
3.  Crea un [**objeto IX500DistinguishedName,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) usa el objeto para codificar el nombre del sujeto en una matriz de bytes y agrega la matriz al objeto de solicitud PKCS \# 10.
4.  Crea un objeto [**IObjectId,**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) lo inicializa mediante el identificador de objeto EKU (OID) especificado en la línea de comandos, crea una colección [**IObjectIds,**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) agrega el nuevo objeto **IObjectId** (EKU) a la colección, usa la colección para inicializar un objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) y agrega este objeto a la solicitud.
5.  Crea un objeto [**IAlternativeName,**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) lo inicializa con el nombre RFC822 especificado en la línea de comandos, crea una colección [**IAlternativeNames,**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) agrega el nuevo objeto **IAlternativeName** (nombre RFC822) a la colección, crea un objeto [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) y agrega este objeto a la solicitud.
6.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante el objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y recupera una cadena que contiene una solicitud codificada en base64.
7.  Crea un [**objeto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de ca.
8.  Crea un objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) y lo usa además de las cadenas que contienen la configuración de ca y la solicitud de certificado para enviar la solicitud a la CA.
9.  Comprueba el estado de envío y, si la inscripción se realiza correctamente, instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
