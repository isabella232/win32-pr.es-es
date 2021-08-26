---
description: El campo asunto de una solicitud de certificado PKCS 10 contiene el nombre distintivo \# de la entidad que solicita el certificado.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nombres de sujeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101114"
---
# <a name="subject-names"></a>Nombres de sujeto

El **campo asunto** de una solicitud de certificado PKCS 10 contiene el nombre distintivo de la entidad que solicita el \# certificado.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

El nombre distintivo consta de una secuencia de nombres distintivos relativos (RDN). Cada RDN consta de un conjunto de atributos y cada atributo consta de un identificador de objeto y un valor. El tipo de datos del valor se identifica mediante la **estructura DirectoryString.**

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

Para obtener más información, vea los temas siguientes:

-   [Crear un nombre de sujeto](creating-a-subject-name.md)
-   [Codificación de un nombre de sujeto](encoding-a-subject-name.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitudes](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
