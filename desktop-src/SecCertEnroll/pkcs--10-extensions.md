---
description: Las extensiones se incluyen en una solicitud de certificado PKCS 10 agregándolos al campo atributos de la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis \# de ASN.1. Para obtener más información, vea el tema Atributos.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: Extensiones PKCS \# 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6db808250b2c3c2a7e29980b115dae3a22f0f37b4912c74332433e2dcf4f2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993285"
---
# <a name="pkcs-10-extensions"></a>Extensiones PKCS \# 10

Las extensiones se incluyen en una solicitud de certificado PKCS 10 agregándolos al campo atributos de la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis \# de ASN.1.   Para obtener más información, vea el [tema Atributos.](attributes.md)

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

En el procedimiento siguiente se describe cómo usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado PKCS \# 10:

1.  Recupere una [**colección IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) llamando a la propiedad [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) en el [**objeto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
2.  Cree una extensión mediante cualquiera de las interfaces disponibles que derivan de la [**interfaz IX509Extension.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
3.  Agregue las extensiones creadas en el paso 2 a la [**colección IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada en el paso 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos](attributes.md)
</dt> <dt>

[Arquitectura de atributos](attribute-architecture.md)
</dt> <dt>

[Atributos PKCS \# 10](pkcs--10-attributes.md)
</dt> <dt>

[Extensiones](extensions.md)
</dt> </dl>

 

 



