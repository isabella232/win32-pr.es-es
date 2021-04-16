---
description: La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar contenido.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificados de clave pública X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571249"
---
# <a name="x509-public-key-certificates"></a>Certificados de clave pública X. 509

La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar contenido. Las claves están relacionadas matemáticamente y el contenido cifrado mediante una de las claves solo se puede descifrar con el otro. La clave privada se mantiene en secreto. Normalmente, la clave pública se incrusta en un certificado binario y el certificado se publica en una base de datos a la que pueden tener acceso todos los usuarios autorizados.

La norma de infraestructura de clave pública (PKI) X. 509 identifica los requisitos de los certificados de clave pública sólidos. Un certificado es una estructura de datos firmada que enlaza una clave pública a una persona, un equipo o una organización. Los certificados los emiten [*las entidades de certificación*](/windows/desktop/SecGloss/c-gly) (CA). Todos los usuarios que son parte de la seguridad de las comunicaciones que hacen uso de una clave pública dependen de la entidad de certificación para comprobar adecuadamente las identidades de los usuarios, sistemas o entidades a los que emite certificados. El nivel de comprobación suele depender del nivel de seguridad necesario para la transacción. Si la entidad de certificación puede comprobar la identidad del solicitante, firma (cifra), codifica y emite el certificado.

Un certificado es una estructura de datos firmada que enlaza una clave pública a una entidad. En el ejemplo siguiente se muestra la sintaxis de la [*notación de sintaxis abstracta uno*](/windows/desktop/SecGloss/a-gly) (ASN. 1) para el certificado de versión 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) .

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

Desde su inicio en 1998, han evolucionado tres versiones del estándar de certificados de clave pública X. 509. Tal y como se muestra en la siguiente ilustración, cada versión sucesiva de la estructura de datos ha retenido los campos que existían en las versiones anteriores y ha agregado más.

![certificados x. 509 versiones 1, 2 y 3](images/x509certificateversions.png)

En los temas siguientes se describen los campos disponibles con más detalle:

-   [Campos básicos](about-basic-fields.md)
-   [Campos de la versión 2](about-version-2-fields.md)
-   [Extensiones de la versión 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura de clave pública](public-key-infrastructure.md)
</dt> </dl>

 

 
