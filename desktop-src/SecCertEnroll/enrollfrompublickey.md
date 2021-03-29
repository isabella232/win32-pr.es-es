---
description: Inicializa un objeto de \# solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud CMC, envía la solicitud CMC a una entidad de certificación (CA) empresarial y guarda el certificado devuelto por la CA en un archivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810694"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

En el ejemplo enrollFromPublicKey se inicializa un \# objeto de solicitud de certificado PKCS 10, se encapsula en un objeto de solicitud CMC, se envía la solicitud CMC a una entidad de certificación (CA) empresarial y se guarda el certificado devuelto por la CA en un archivo.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey

## <a name="discussion"></a>Debate

El ejemplo enrollFromPublicKey:

1.  Procesa los siguientes argumentos de la línea de comandos:
    -   Nombre de una plantilla de certificado.
    -   Nombre de un archivo en el que se va a guardar el certificado instalado como una matriz de bytes codificada en Base64.
    -   Nombre opcional de la plantilla de certificado de firma. La plantilla se usa para crear un certificado de firma si no existe ninguno en el almacén de certificados.
2.  Crea un objeto de clave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y llama al método [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) para crear una clave privada asimétrica con el proveedor de servicios criptográficos, el tamaño de clave y los valores de [**especificación**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) de clave predeterminados para el equipo actual.
3.  Recupera la parte de la clave pública del objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .
4.  Crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo Inicializa utilizando la plantilla especificada en la línea de comandos y la clave pública.
5.  Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el \# objeto de solicitud PKCS 10.
6.  Recupera un certificado de firma existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirla. FindCertByKeyUsage se define en enrollCommon. cpp.
7.  Comprueba la cadena de certificados.
8.  Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de firma, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud CMC y agrega el objeto de certificado de firma a la colección.
9.  Codifica la solicitud CMC mediante [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der).
10. Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
11. Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.
12. Comprueba el estado del proceso de inscripción y guarda el certificado instalado en un archivo. La función EncodeToFileW se define en enrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
