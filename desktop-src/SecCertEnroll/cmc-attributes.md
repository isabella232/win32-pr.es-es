---
description: En la práctica, la estructura de una solicitud de CMC, mostrada por la sintaxis siguiente, es relativamente compleja porque a menudo contiene solicitudes anidadas.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Atributos de CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b98e30c257234ebee864a1749ceecee7b79e25a9e11c9f1f190c60f3154ef64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902068"
---
# <a name="cmc-attributes"></a>Atributos de CMC

En la práctica, la estructura de una solicitud de CMC, mostrada por la sintaxis siguiente, es relativamente compleja porque a menudo contiene solicitudes anidadas. Por ejemplo, una solicitud CMC puede contener cero o una solicitud PKCS 10 en una secuencia TaggedRequest y puede contener cero o un mensaje PKCS 7 en una secuencia \#  \# **TaggedContentInfo.** Cada mensaje PKCS \# 7 anidado puede contener una solicitud de CMC que, a su vez, puede contener más solicitudes. El número de niveles de anidamiento es teóricamente ilimitado, pero la entidad de certificación (CA) normalmente está configurada para limitar el tamaño de una solicitud. Los atributos se pueden aplicar a la solicitud de nivel superior o a las solicitudes anidadas. Esto se describe en las secciones siguientes.

## <a name="cmcdata-structure"></a>CMCData (estructura)

Una solicitud de CMC contiene secuencias de estructuras **TAGGEDAttribute,** **TaggedRequest** y **TaggedContentInfo** ASN.1.

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a>TaggedAttribute (estructura)

Los atributos se incluyen en una solicitud de certificado de CMC agregándolos a la **colección TaggedAttribute.** Cada estructura de la colección contiene un identificador entero, un identificador de objeto ASN.1 (OID) y un conjunto de valores. Los valores posibles pueden ser cualquiera de los siguientes.

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a>CMCAddAttributes

Si los atributos de esta estructura se aplican a una solicitud PKCS \# 10 anidada, el **campo certReferences** contendrá **bodyPartID** que identifica la solicitud. Si los atributos se aplican a una solicitud DE CMC anidada, el **campo pkiDataReference** contendrá el **BodyPartID** de la solicitud. Actualmente, solo uno de estos campos puede ser distinto de cero. Los atributos que se pueden incluir se enumeran en el [tema Atributos admitidos.](supported-attributes.md)

## <a name="cmcaddextensions"></a>CmcAddExtensions

Esta estructura puede contener extensiones X.509 versión 3 más las extensiones definidas por Microsoft. Este atributo se define mediante la [**interfaz IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Si las extensiones se aplican a una solicitud PKCS \# 10 anidada, el **campo certReferences** contendrá **bodyPartID** que identifica la solicitud. Si las extensiones se aplican a una solicitud DE CMC anidada, el **campo pkiDataReference** contendrá el **BodyPartID** de la solicitud. Actualmente, solo uno de estos campos puede ser distinto de cero.

## <a name="sendernonce"></a>SenderNonce

Un valor nonce son datos binarios aleatorios o pseudo aleatorios que se pueden incluir en una solicitud de certificado y una transacción de respuesta para ayudar a garantizar que la respuesta o la solicitud no es una repetición de un mensaje anterior. Para obtener más información, vea la [**propiedad SenderNonce.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce)

## <a name="transactid"></a>TransactID

Se puede realizar un seguimiento de una solicitud de certificado de ida y vuelta y una transacción de respuesta mediante un identificador. El cliente genera un identificador de transacción y lo conserva hasta que la entidad de registro o el certificado responda con un mensaje que complete la transacción. La respuesta incluye el identificador. Para obtener más información, vea la [**propiedad TransactionId.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid)

## <a name="reginfo"></a>RegInfo

Este atributo se puede usar para contener cualquier información de registro que el cliente decida incluir en la solicitud de CMC. El valor del atributo es una cadena que contiene pares nombre-valor concatenados. Para obtener más información, vea la [**propiedad NameValuePairs.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos compatibles](supported-attributes.md)
</dt> </dl>

 

 



