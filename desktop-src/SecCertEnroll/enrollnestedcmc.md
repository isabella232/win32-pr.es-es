---
description: Lee una solicitud de certificado de CMC existente de un archivo, la encapsula en otra solicitud de CMC, firma esta solicitud externa, la envía a una entidad de certificación (CA) y guarda la respuesta del certificado de la CA en un archivo.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882945"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

El ejemplo enrollNestedCMC lee una solicitud de certificado de CMC existente de un archivo, la encapsula en otra solicitud de CMC, firma esta solicitud externa, la envía a una entidad de certificación (CA) y guarda la respuesta del certificado de la ca en un archivo.

## <a name="location"></a>Ubicación

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta enrollNestedCMC *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples \\ X509 Certificate Enrollment \\ VC \\ enrollNestedCMC .

## <a name="discussion"></a>Debate

El ejemplo enrollNestedCMC:

1.  Procesa los siguientes argumentos de línea de comandos:
    -   Nombre del archivo de entrada.
    -   Nombre del archivo de salida.
    -   Plantilla de solicitud opcional.
2.  Lee una solicitud de CMC existente de un archivo como una matriz de bytes codificada en base63, convierte la matriz de bytes en **un BSTR,** crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y usa **el BSTR** para inicializar el objeto de solicitud. El objeto inicializado se convierte en la solicitud interna.
3.  Usa el objeto de solicitud interno creado e inicializado en el paso anterior para inicializar otra solicitud de CMC.
4.  Recupera un certificado de firma existente o, si no se encuentra uno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirlo. Las funciones findCertByTemplate e enrollCertByTemplate se definen en enrollCommon.cpp.
5.  Recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de la solicitud CMC externa, crea un nuevo objeto [**ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inicializa mediante el certificado de firma recuperado y lo agrega a la colección.
6.  Codifica la solicitud de CMC mediante reglas de codificación distinguida (DER) y recupera la solicitud como **un BSTR**.
7.  Crea un [**objeto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de ca.
8.  Crea un objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) y lo usa además de las cadenas que contienen la configuración de ca y la solicitud de certificado para enviar la solicitud a la CA.
9.  Comprueba el estado del proceso de inscripción y guarda la respuesta del certificado de la entidad de certificación en un archivo. La función EncodeToFileW se define en enrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
