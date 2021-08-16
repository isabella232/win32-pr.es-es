---
description: Inicializa un objeto de solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud de CMC, envía la solicitud de CMC a una entidad de certificación (CA) empresarial y guarda el certificado devuelto por la CA en un \# archivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780054"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

El ejemplo enrollFromPublicKey inicializa un objeto de solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud de CMC, envía la solicitud de CMC a una entidad de certificación (CA) empresarial y guarda el certificado devuelto por la CA en un \# archivo.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala de forma predeterminada en la carpeta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey .

## <a name="discussion"></a>Debate

El ejemplo enrollFromPublicKey:

1.  Procesa los siguientes argumentos de línea de comandos:
    -   Nombre de una plantilla de certificado.
    -   Nombre de un archivo en el que se va a guardar el certificado instalado como una matriz de bytes codificada en base64.
    -   Un nombre de plantilla de certificado de firma opcional. La plantilla se usa para crear un certificado de firma si no existe ninguno en el almacén de certificados.
2.  Crea un objeto de clave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y llama al método [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) para crear una clave privada asimétrica con los valores predeterminados de proveedor criptográfico, tamaño de clave y [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) para el equipo actual.
3.  Recupera la parte de clave pública del [**objeto IX509PrivateKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
4.  Crea un [**objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante la plantilla especificada en la línea de comandos y la clave pública.
5.  Crea un [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el objeto de solicitud PKCS \# 10.
6.  Recupera un certificado de firma existente o, si no se encuentra uno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirlo. FindCertByKeyUsage se define en enrollCommon.cpp.
7.  Comprueba la cadena de certificados.
8.  Crea un [**objeto ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inicializa mediante el certificado de firma, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud de CMC y agrega el objeto de certificado de firma a la colección.
9.  Codifica la solicitud de CMC mediante [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (DER).
10. Crea un [**objeto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de ca.
11. Crea un objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) y lo usa además de las cadenas que contienen la configuración de ca y la solicitud de certificado para enviar la solicitud a la CA.
12. Comprueba el estado del proceso de inscripción y guarda el certificado instalado en un archivo. La función EncodeToFileW se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
