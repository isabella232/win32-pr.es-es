---
description: Crea una solicitud PKCS \# 10 personalizada, la envía a una entidad de certificación (CA) independiente y lo instala en el almacén de certificados.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648221"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

El ejemplo enrollCustomPKCS10 crea una solicitud PKCS \# 10 personalizada, la envía a una entidad de certificación (CA) independiente y lo instala en el almacén de certificados. Una CA independiente no requiere Active Directory y no utiliza plantillas.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10

## <a name="discussion"></a>Debate

El ejemplo enrollCustomPKCS10:

1.  Procesa los argumentos de la línea de comandos. La línea de comandos debe contener el nombre de sujeto del certificado X. 500, el nombre de correo electrónico (RFC822) y un identificador de objeto (OID) de uso mejorado de clave (EKU). Por ejemplo, puede especificar los argumentos siguientes para inscribirse *user1@example.com* :
    -   Nombre del firmante: "*CN = user1, DC = ejemplo, DC = com*"
    -   Nombre de RFC822: *user1@example.com*
    -   OID de EKU de autenticación de cliente: 1.3.6.1.5.5.7.3.2
2.  Crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa para el usuario final especificando el valor **ContextUser** de la enumeración [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) .
3.  Crea un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , usa el objeto para codificar el nombre del sujeto en una matriz de bytes y agrega la matriz al \# objeto de solicitud PKCS 10.
4.  Crea un objeto [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , lo inicializa con el identificador de objeto EKU (OID) especificado en la línea de comandos, crea una colección [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) , agrega el nuevo objeto **IObjectId** (EKU) a la colección, utiliza la colección para inicializar un objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) y agrega este objeto a la solicitud.
5.  Crea un objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , lo inicializa con el nombre RFC822 especificado en la línea de comandos, crea una colección [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , agrega el nuevo objeto **IAlternativeName** (nombre RFC822) a la colección, crea un objeto [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) y agrega este objeto a la solicitud.
6.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y recupera una cadena que contiene una solicitud codificada en Base64.
7.  Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
8.  Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.
9.  Comprueba el estado de envío y, si la inscripción se realiza correctamente, instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
