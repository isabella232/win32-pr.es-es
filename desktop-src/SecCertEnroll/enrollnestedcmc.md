---
description: Lee una solicitud de certificado CMC existente desde un archivo, la incluye en otra solicitud CMC, firma esta solicitud externa, la envía a una entidad de certificación (CA) y guarda la respuesta del certificado de la CA en un archivo.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275210"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

En el ejemplo enrollNestedCMC se lee una solicitud de certificado CMC existente desde un archivo, se incluye en otra solicitud CMC, se firma esta solicitud externa, se envía a una entidad de certificación (CA) y se guarda la respuesta del certificado de la CA en un archivo.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples enrollNestedCMC de la \\ inscripción de certificados de \\ VC \\ .

## <a name="discussion"></a>Debate

El ejemplo enrollNestedCMC:

1.  Procesa los siguientes argumentos de la línea de comandos:
    -   Nombre del archivo de entrada.
    -   Nombre del archivo de salida.
    -   Una plantilla de solicitud opcional.
2.  Lee una solicitud CMC existente desde un archivo como una matriz de bytes codificada en base63, convierte la matriz de bytes en un **BSTR**, crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y usa **BSTR** para inicializar el objeto de solicitud. El objeto inicializado se convierte en la solicitud interna.
3.  Usa el objeto de solicitud interno creado e inicializado en el paso anterior para inicializar otra solicitud de CMC.
4.  Recupera un certificado de firma existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirla. Las funciones findCertByTemplate y enrollCertByTemplate se definen en enrollCommon. cpp.
5.  Recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de la solicitud CMC externa, crea un nuevo objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de firma recuperado y lo agrega a la colección.
6.  Codifica la solicitud CMC mediante reglas de codificación distinguida (DER) y recupera la solicitud como **BSTR**.
7.  Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.
8.  Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.
9.  Comprueba el estado del proceso de inscripción y guarda la respuesta del certificado de la CA en un archivo. La función EncodeToFileW se define en enrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> </dl>

 

 
