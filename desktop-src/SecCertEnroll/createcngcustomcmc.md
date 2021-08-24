---
description: Crea un objeto de solicitud de CMC a partir de una solicitud PKCS \# 10 anidada interna.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0494fdf2af9e4e96983ed1aff462b38e749516eafe87f645a3bf8ae1b342292d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798275"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

El ejemplo createCNGCustomCMC crea un objeto de solicitud cmc a partir de una solicitud PKCS \# 10 anidada interna. La solicitud interna se crea mediante una clave [*privada asimétrica*](/windows/desktop/SecGloss/p-gly). La clave privada se crea mediante el proveedor criptográfico Cryptography API: Next Generation (CNG) y el algoritmo especificado en la línea de comandos. Las opciones personalizadas, como la directiva de exportación y el nivel de protección de claves, también se establecen en la clave privada.

## <a name="location"></a>Location

Al instalar el Kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta createCNGCustomCMC de *%ProgramFiles%* de los SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ createCNGCustomCMC.

## <a name="discussion"></a>Debate

El ejemplo createCNGCustomCMC:

1.  Procesa los siguientes argumentos de línea de comandos:
    -   Nombre de un proveedor de servicios [*criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) de CNG.
    -   Nombre del algoritmo utilizado para generar una clave privada asimétrica.
    -   Nombre del algoritmo utilizado para la solicitud [*de certificado.*](/windows/desktop/SecGloss/h-gly) [](/windows/desktop/SecGloss/c-gly)
    -   Archivo de salida en el que se va a guardar la solicitud de certificado.
    -   Cadena opcional (AlternateSignature) que, si está presente, especifica que se usará un algoritmo de firma discreto en lugar de un algoritmo de firma combinado. Para obtener más información, vea [**la propiedad AlternateSignatureAlgorithm.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)
2.  Crea un [**objeto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y establece las siguientes propiedades:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algoritmo**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**KeyProtection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Crea una clave privada asimétrica.
4.  Crea un [**objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa mediante la clave privada.
5.  Crea un [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e inicializa mediante el objeto de solicitud PKCS \# 10 creado en el paso 4.
6.  Establece la marca del algoritmo de firma alternativo **en VARIANT \_ TRUE** o **VARIANT \_ FALSE** en función de si se especifica una cadena de firma alternativa en la línea de comandos. Para obtener más información, [**vea AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Crea un [*identificador de objeto*](/windows/desktop/SecGloss/h-gly) [*de*](/windows/desktop/SecGloss/o-gly) algoritmo hash (OID) a partir del nombre del algoritmo especificado en la línea de comandos y establece el OID en el objeto de solicitud de CMC.
8.  Firma la solicitud de certificado y la codifica [*mediante reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (DER).
9.  Recupera una cadena que contiene la solicitud de certificado CMC codificada y la guarda en un archivo. La función EncodeToFileW se define en EnrollCommon.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de CMC](cmc-request.md)
</dt> <dt>

[Solicitud PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso de los ejemplos incluidos](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
