---
description: Las extensiones se incluyen en una solicitud CMC agregándolas a la estructura TaggedAttributes que se muestra en el siguiente ejemplo de sintaxis ASN. 1. Para obtener más información, vea el tema atributos.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensiones de CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277963"
---
# <a name="cmc-extensions"></a>Extensiones de CMC

Las extensiones se incluyen en una solicitud CMC agregándolas a la estructura **TaggedAttributes** que se muestra en el siguiente ejemplo de sintaxis ASN. 1. Para obtener más información, vea el tema [atributos](attributes.md) .

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

Cada estructura de la colección **TaggedAttributes** contiene un identificador entero, un identificador de objeto ASN. 1 (OID) y un conjunto de valores. Las extensiones se incorporan en una solicitud agregando una estructura **CmcAddExtensions** al campo **valores** . En el ejemplo siguiente se muestra la sintaxis de la estructura ASN. 1. El identificador de objeto es **XCN \_ OID \_ CMC \_ Add \_ extensions** (1.3.6.1.5.5.7.7.8).

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

En el procedimiento siguiente se describe cómo usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado CMC.

**Para usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado CMC**

1.  Cree una extensión mediante cualquiera de las interfaces disponibles que derivan de la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) o use el objeto **IX509Extension** directamente para crear extensiones personalizadas.
2.  Llame a la propiedad [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) del objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para recuperar una colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
3.  Agregue las extensiones creadas en el paso 1 a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
4.  Llame a [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para realizar automáticamente las siguientes acciones:
    -   Recupere un objeto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) del objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
    -   Cree e inicialice un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) mediante la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada en el paso 2.
    -   Cree una colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) y agréguele el objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .
    -   Use la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
    -   Agregue el objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos](attributes.md)
</dt> <dt>

[Arquitectura de atributo](attribute-architecture.md)
</dt> <dt>

[Atributos de CMC](cmc-attributes.md)
</dt> <dt>

[Extensiones](extensions.md)
</dt> </dl>

 

 



