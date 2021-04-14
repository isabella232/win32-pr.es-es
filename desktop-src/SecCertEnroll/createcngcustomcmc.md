---
description: Crea un objeto de solicitud CMC a partir de una solicitud PKCS 10 anidada interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360145"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

En el ejemplo createCNGCustomCMC se crea un objeto de solicitud CMC a partir de una solicitud anidada PKCS \# 10 interna. La solicitud interna se crea con una [*clave privada*](/windows/desktop/SecGloss/p-gly)asimétrica. La clave privada se crea mediante el proveedor criptográfico Cryptography API: Next Generation (CNG) y el algoritmo especificado en la línea de comandos. También se establecen opciones personalizadas como la Directiva de exportación y el nivel de protección de claves en la clave privada.

## <a name="location"></a>Location

Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ createCNGCustomCMC

## <a name="discussion"></a>Debate

El ejemplo createCNGCustomCMC:

1.  Procesa los siguientes argumentos de la línea de comandos:
    -   Nombre de un proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) de CNG.
    -   Nombre del algoritmo utilizado para generar una clave privada asimétrica.
    -   Nombre del algoritmo utilizado para aplicar un algoritmo [*hash*](/windows/desktop/SecGloss/h-gly) a la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly).
    -   Archivo de salida en el que se va a guardar la solicitud de certificado.
    -   Una cadena opcional (AlternateSignature) que, si está presente, especifica que se use un algoritmo de firma discreto en lugar de uno combinado. Para obtener más información, vea la propiedad [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .
2.  Crea un objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y establece las siguientes propiedades:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algoritmo**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**KeyProtection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Crea una clave privada asimétrica.
4.  Crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante la clave privada.
5.  Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el \# objeto de solicitud PKCS 10 creado en el paso 4.
6.  Establece la marca de algoritmo de firma alternativa en **Variant \_ true** o **Variant \_ false** en función de si se ha especificado una cadena de firma alternativa en la línea de comandos. Para obtener más información, vea [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Crea un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) de [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) (OID) a partir del nombre del algoritmo especificado en la línea de comandos y establece el OID en el objeto de solicitud CMC.
8.  Firma la solicitud de certificado y la codifica mediante [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der).
9.  Recupera una cadena que contiene la solicitud de certificado CMC codificada y la guarda en un archivo. La función EncodeToFileW se define en EnrollCommon. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitud PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usar los ejemplos incluidos](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
