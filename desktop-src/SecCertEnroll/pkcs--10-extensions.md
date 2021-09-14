---
description: Las extensiones se incluyen en una solicitud de certificado PKCS 10 agregándolos al campo de atributos de la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis \# de ASN.1. Para obtener más información, vea el tema Atributos.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: Extensiones PKCS \# 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171197"
---
# <a name="pkcs-10-extensions"></a>Extensiones PKCS \# 10

Las extensiones se incluyen en una solicitud de certificado PKCS 10 agregándolos al campo de atributos de la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis \# de ASN.1.   Para obtener más información, vea el [tema Atributos.](attributes.md)

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

 

 



