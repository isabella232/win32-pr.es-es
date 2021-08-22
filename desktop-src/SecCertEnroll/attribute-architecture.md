---
description: Se usa para agregar atributos a una solicitud de certificado.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Arquitectura de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d09a2a351635547c21357477290cb3335cb8c1da042d680762140b48b03f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903242"
---
# <a name="attribute-architecture"></a>Arquitectura de atributos

Las interfaces siguientes se usan para agregar atributos a una solicitud de certificado:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

La arquitectura sigue a la definida en el módulo ASN.1 de la sintaxis de solicitud de certificación PKCS \# 10.

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

La [**colección ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) corresponde al campo **attributes** y cada objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) de la colección corresponde a una estructura de atributo ASN.1. 

Cada **atributo** consta de un identificador de objeto (OID) y cero o más valores asociados al OID. Un único par OID-valor se representa mediante una [**interfaz IX509Attribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) Puede usar una [**colección IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un objeto [**ICryptAttribute,**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) pero cada atributo de la colección debe estar asociado al mismo OID. Normalmente, un atributo solo tiene un valor.

Puede usar cualquiera de las interfaces siguientes, que derivan de [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), para crear un único par de atributos OID/valor:

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Por ejemplo, el procedimiento siguiente muestra cómo crear un atributo **ClientId.**

**Para crear un **atributo ClientId****

1.  Recupere un [**objeto ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) de un [**objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) [**o IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
2.  Cree e inicialice [**un objeto IX509AttributeClientId.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
3.  Cree una [**colección IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) y agregue el [**objeto IX509AttributeClientId.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
4.  Use la [**colección IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un [**objeto ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
5.  Agregue el [**objeto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la colección recuperada en el paso 1.

En el ejemplo siguiente se muestra la salida asn.1 del **atributo ClientId.** El atributo contiene el nombre DNS del equipo en el que se generó la solicitud (test3d.jdomcsc.nttest.microsoft.com), el nombre SAM del usuario (administrador de JDOMCSC) y el nombre de la aplicación que generó la solicitud \\ (certreq).

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



