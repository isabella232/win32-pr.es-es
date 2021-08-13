---
description: Las extensiones se incluyen en una solicitud de CMC agregándolos a la estructura TaggedAttributes que se muestra en el siguiente ejemplo de sintaxis de ASN.1. Para obtener más información, vea el tema Atributos.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensiones de CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d29873bc43f7a7229b363a7b09cdf03a23127cc5d5e0e738036c6005a6cc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901848"
---
# <a name="cmc-extensions"></a>Extensiones de CMC

Las extensiones se incluyen en una solicitud de CMC agregándolos a la estructura **TaggedAttributes** que se muestra en el siguiente ejemplo de sintaxis de ASN.1. Para obtener más información, vea el [tema Atributos.](attributes.md)

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Cada estructura de la **colección TaggedAttributes** contiene un identificador entero, un identificador de objeto ASN.1 (OID) y un conjunto de valores. Las extensiones se incorporan en una solicitud agregando una **estructura CmcAddExtensions** al **campo values.** La sintaxis de la estructura ASN.1 se muestra en el ejemplo siguiente. El identificador de objeto **es XCN \_ OID \_ CMC \_ ADD \_ EXTENSIONS** (1.3.6.1.5.5.7.7.8).

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

En el procedimiento siguiente se describe cómo usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado de CMC.

**Para usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado de CMC**

1.  Cree una extensión mediante cualquiera de las interfaces disponibles que derivan de la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) o use el objeto **IX509Extension** directamente para crear extensiones personalizadas.
2.  Llame a [**la propiedad X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) en el [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para recuperar una [**colección IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
3.  Agregue las extensiones creadas en el paso 1 a la [**colección IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
4.  Llame [**a Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para realizar automáticamente las siguientes acciones:
    -   Recupere un [**objeto ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) del [**objeto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
    -   Cree e inicialice [**un objeto IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) mediante la [**colección IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada en el paso 2.
    -   Cree una [**colección IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) y agréle [**el objeto IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
    -   Use la [**colección IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un [**objeto ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
    -   Agregue el [**objeto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la [**colección ICryptAttributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos](attributes.md)
</dt> <dt>

[Arquitectura de atributos](attribute-architecture.md)
</dt> <dt>

[Atributos de CMC](cmc-attributes.md)
</dt> <dt>

[Extensiones](extensions.md)
</dt> </dl>

 

 



