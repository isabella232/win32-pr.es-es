---
description: Crea una solicitud de certificado de CMC e inscribe un equipo en una jerarquía de certificados.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799cd70d8f3b70ae32a95b7720a879ddd611fba5e35064d1794d39bdcd7ab9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780064"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

El ejemplo enrollCustomCMC crea una solicitud de certificado de CMC e inscribe un equipo en una jerarquía de certificados.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *%ProgramFiles%* \\ microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomCMC .

## <a name="discussion"></a>Debate

El ejemplo enrollCustomCMC:

1.  Procesa los siguientes argumentos de línea de comandos:
    -   Par nombre-valor personalizado que se agregará a la solicitud de certificado.
    -   Un nombre de sujeto alternativo.
    -   Identificador de objeto (OID) para la extensión Uso mejorado de clave (EKU).
2.  Crea un [**objeto de solicitud IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante el contexto del equipo.
3.  Usa la solicitud PKCS \# 10 para inicializar un [**objeto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
4.  Crea un [**objeto IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) mediante el OID especificado en la línea de comandos y lo agrega a la colección de extensiones para la solicitud de CMC.
5.  Crea el objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) con el nombre especificado en la línea de comandos, lo agrega a la colección [**IAlternativeNames,**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) usa la colección para inicializar una extensión [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) y la agrega a la colección de extensiones para la solicitud de CMC.
6.  Crea un objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) utilizando el nombre y el valor especificados en la línea de comandos, y lo agrega a la colección [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) en la solicitud de CMC.
7.  Crea un [**objeto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inicializa mediante el objeto de solicitud CMC y recupera una cadena que contiene una solicitud codificada en base64.
8.  Crea un [**objeto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
9.  Crea un objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) y lo usa además de las cadenas que contienen la configuración de ca y la solicitud de certificado para enviar la solicitud a la CA.
10. Comprueba el estado de envío y, si se realiza correctamente, instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
