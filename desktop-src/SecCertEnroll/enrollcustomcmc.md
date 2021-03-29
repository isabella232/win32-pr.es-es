---
description: Crea una solicitud de certificado CMC e inscribe un equipo en una jerarquía de certificados.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810700"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

El ejemplo enrollCustomCMC crea una solicitud de certificado CMC e inscribe un equipo en una jerarquía de certificados.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCustomCMC

## <a name="discussion"></a>Debate

El ejemplo enrollCustomCMC:

1.  Procesa los siguientes argumentos de la línea de comandos:
    -   Par de nombre y valor personalizado que se va a agregar a la solicitud de certificado.
    -   Un nombre de sujeto alternativo.
    -   Identificador de objeto (OID) para la extensión uso mejorado de clave (EKU).
2.  Crea un objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante el contexto de equipo.
3.  Usa la \# solicitud PKCS 10 para inicializar un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
4.  Crea un objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) mediante el OID especificado en la línea de comandos y lo agrega a la colección de extensiones para la solicitud CMC.
5.  Crea el objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) con el nombre especificado en la línea de comandos, lo agrega a la colección [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa la colección para inicializar una extensión [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) y lo agrega a la colección de extensiones para la solicitud CMC.
6.  Crea un objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) con el nombre y el valor especificados en la línea de comandos y lo agrega a la colección [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) en la solicitud CMC.
7.  Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el objeto de solicitud CMC y recupera una cadena que contiene una solicitud codificada en Base64.
8.  Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
9.  Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.
10. Comprueba el estado de envío y, si se realiza correctamente, instala el certificado en el almacén de certificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
