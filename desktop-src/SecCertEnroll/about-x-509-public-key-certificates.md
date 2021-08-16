---
description: La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar el contenido.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificados de clave pública X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1eb40e57114f4509884df3a5ac36e7ae8ea0486817ff300d58f4273d51c123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903262"
---
# <a name="x509-public-key-certificates"></a>Certificados de clave pública X.509

La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar el contenido. Las claves están relacionadas matemáticamente y el contenido cifrado mediante una de las claves solo se puede descifrar mediante el otro. La clave privada se mantiene en secreto. La clave pública se incrusta normalmente en un certificado binario y el certificado se publica en una base de datos a la que pueden acceder todos los usuarios autorizados.

El estándar de infraestructura de clave pública (PKI) X.509 identifica los requisitos para certificados de clave pública sólidos. Un certificado es una estructura de datos firmada que enlaza una clave pública a una persona, equipo u organización. Las entidades de [](/windows/desktop/SecGloss/c-gly) certificación (CA) emiten certificados. Todos los usuarios que son parte de la protección de las comunicaciones que usan una clave pública dependen de la entidad de certificación para comprobar adecuadamente las identidades de las personas, sistemas o entidades a los que emite certificados. El nivel de comprobación normalmente depende del nivel de seguridad necesario para la transacción. Si la ca puede comprobar adecuadamente la identidad del solicitante, firma (cifra), codifica y emite el certificado.

Un certificado es una estructura de datos firmada que enlaza una clave pública a una entidad. La [*sintaxis abstracta Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) para el certificado [*X.509*](/windows/desktop/SecGloss/x-gly) de la versión 3 se muestra en el ejemplo siguiente.

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

Desde su creación en 1998, han evolucionado tres versiones del estándar de certificado de clave pública X.509. Como se muestra en la ilustración siguiente, cada versión sucesiva de la estructura de datos ha conservado los campos que existían en las versiones anteriores y ha agregado más.

![Certificados x.509 versiones 1, 2 y 3](images/x509certificateversions.png)

En los temas siguientes se tratan los campos disponibles con más detalle:

-   [Campos básicos](about-basic-fields.md)
-   [Campos de la versión 2](about-version-2-fields.md)
-   [Extensiones de la versión 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura de clave pública](public-key-infrastructure.md)
</dt> </dl>

 

 
