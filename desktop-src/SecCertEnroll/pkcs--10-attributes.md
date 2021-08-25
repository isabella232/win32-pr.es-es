---
description: Los atributos se incluyen en una solicitud de certificado PKCS 10 agregándolos a la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de \# sintaxis de ASN.1.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: Atributos PKCS \# 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993295"
---
# <a name="pkcs-10-attributes"></a>Atributos PKCS \# 10

Los atributos se incluyen en una solicitud de certificado PKCS 10 agregándolos a la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de \# sintaxis de  ASN.1. Para obtener más información sobre cómo puede agregar atributos a una solicitud, vea el tema [Arquitectura de](attribute-architecture.md) atributos.

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

El atributo que se agrega normalmente a una solicitud PKCS 10 es una colección de extensiones de la versión 3 definidas por un \# [**objeto IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Dado que una solicitud PKCS 10 no contiene un campo al que se pueden agregar directamente las extensiones, deben agregarse \# como atributo. Los **atributos ClientId**, **CspProvider**, **OSVersion** y **RenewalCertificate** también se pueden agregar a un tema PKCS ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos compatibles](supported-attributes.md)
</dt> </dl>

 

 



