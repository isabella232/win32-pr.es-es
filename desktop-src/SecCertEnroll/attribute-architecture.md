---
description: Se utiliza para agregar atributos a una solicitud de certificado.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Arquitectura de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360589"
---
# <a name="attribute-architecture"></a><span data-ttu-id="73e0c-103">Arquitectura de atributo</span><span class="sxs-lookup"><span data-stu-id="73e0c-103">Attribute Architecture</span></span>

<span data-ttu-id="73e0c-104">Las siguientes interfaces se usan para agregar atributos a una solicitud de certificado:</span><span class="sxs-lookup"><span data-stu-id="73e0c-104">The following interfaces are used to add attributes to a certificate request:</span></span>

-   [<span data-ttu-id="73e0c-105">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="73e0c-105">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="73e0c-106">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="73e0c-106">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="73e0c-107">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="73e0c-107">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="73e0c-108">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="73e0c-108">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

<span data-ttu-id="73e0c-109">La arquitectura sigue los definidos en el módulo ASN. 1 de la \# Sintaxis de solicitud de certificación PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="73e0c-109">The architecture follows that defined in the ASN.1 module of the PKCS \#10 certification request syntax.</span></span>

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

<span data-ttu-id="73e0c-110">La colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) se corresponde con el campo **attributes** , y cada objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) de la colección corresponde a una estructura de **atributo** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="73e0c-110">The [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection corresponds to the **attributes** field, and each [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object in the collection corresponds to an ASN.1 **Attribute** structure.</span></span>

<span data-ttu-id="73e0c-111">Cada **atributo** consta de un identificador de objeto (OID) y cero o más valores asociados con el OID.</span><span class="sxs-lookup"><span data-stu-id="73e0c-111">Each **Attribute** consists of an object identifier (OID) and zero or more values associated with the OID.</span></span> <span data-ttu-id="73e0c-112">Un par de valor OID único se representa mediante una interfaz [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="73e0c-112">A single OID-value pair is represented by an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) interface.</span></span> <span data-ttu-id="73e0c-113">Puede usar una colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) , pero cada atributo de la colección debe estar asociado al mismo OID.</span><span class="sxs-lookup"><span data-stu-id="73e0c-113">You can use an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object, but each attribute in the collection must be associated with the same OID.</span></span> <span data-ttu-id="73e0c-114">Normalmente, un atributo solo tiene un valor.</span><span class="sxs-lookup"><span data-stu-id="73e0c-114">Typically, an attribute has only one value.</span></span>

<span data-ttu-id="73e0c-115">Puede utilizar cualquiera de las siguientes interfaces, que derivan de [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), para crear un par de atributo Oid/Value único:</span><span class="sxs-lookup"><span data-stu-id="73e0c-115">You can use any of the following interfaces, which derive from [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), to create a single OID/value attribute pair:</span></span>

-   [<span data-ttu-id="73e0c-116">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="73e0c-116">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="73e0c-117">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="73e0c-117">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="73e0c-118">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="73e0c-118">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="73e0c-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="73e0c-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="73e0c-120">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="73e0c-120">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="73e0c-121">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="73e0c-121">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="73e0c-122">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="73e0c-122">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="73e0c-123">Por ejemplo, en el siguiente procedimiento se muestra cómo crear un atributo **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="73e0c-123">For example, the following procedure shows how to create a **ClientId** attribute.</span></span>

<span data-ttu-id="73e0c-124">\*\*Para crear un atributo \*\*ClientID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="73e0c-124">**To create a **ClientId** attribute**</span></span>

1.  <span data-ttu-id="73e0c-125">Recupera un objeto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) de un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="73e0c-125">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
2.  <span data-ttu-id="73e0c-126">Cree e inicialice un objeto [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="73e0c-126">Create and initialize an [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
3.  <span data-ttu-id="73e0c-127">Cree una colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) y agregue el objeto [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="73e0c-127">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
4.  <span data-ttu-id="73e0c-128">Use la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="73e0c-128">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
5.  <span data-ttu-id="73e0c-129">Agregue el objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la colección recuperada en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="73e0c-129">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the collection retrieved in step 1.</span></span>

<span data-ttu-id="73e0c-130">En el ejemplo siguiente se muestra la salida ASN. 1 del atributo **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="73e0c-130">The following example shows the ASN.1 output of the **ClientId** attribute.</span></span> <span data-ttu-id="73e0c-131">El atributo contiene el nombre DNS del equipo en el que se generó la solicitud (test3d.jdomcsc.nttest.microsoft.com), el nombre de SAM del usuario (Administrador de JDOMCSC \\ ) y el nombre de la aplicación que generó la solicitud (CertReq).</span><span class="sxs-lookup"><span data-stu-id="73e0c-131">The attribute contains the DNS name of the computer on which the request was generated (test3d.jdomcsc.nttest.microsoft.com), the SAM name of the user (JDOMCSC\\administrator), and the name of the application that generated the request (certreq).</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="73e0c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73e0c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e0c-133">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="73e0c-133">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="73e0c-134">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="73e0c-134">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="73e0c-135">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="73e0c-135">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="73e0c-136">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="73e0c-136">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



