---
description: Los atributos se incluyen en una \# solicitud de certificado PKCS 10 agregándolas a la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis ASN. 1.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Atributos PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361636"
---
# <a name="pkcs-10-attributes"></a>\#Atributos PKCS 10

Los atributos se incluyen en una \# solicitud de certificado PKCS 10 agregándolas a la estructura **CertificationRequestInfo** que se muestra en el siguiente ejemplo de sintaxis ASN. 1. Para obtener más información sobre cómo puede agregar atributos a una solicitud, vea el tema sobre la [arquitectura de atributo](attribute-architecture.md) .

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

El atributo que se agrega normalmente a una \# solicitud PKCS 10 es una colección de extensiones de la versión 3 definida por un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Dado que una \# solicitud PKCS 10 no contiene un campo al que se puedan agregar las extensiones directamente, deben agregarse como atributo. Los atributos **ClientID**, **CspProvider**, **OSVersion** y **RenewalCertificate** también se pueden agregar a un archivo PKCS).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos compatibles](supported-attributes.md)
</dt> </dl>

 

 



