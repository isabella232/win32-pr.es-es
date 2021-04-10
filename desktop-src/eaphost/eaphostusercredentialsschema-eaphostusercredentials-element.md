---
title: Elemento EapHostUserCredentials
description: Contiene el elemento EapMethod, las credenciales o el elemento CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Elemento EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150683"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="cc746-104">Elemento EapHostUserCredentials</span><span class="sxs-lookup"><span data-stu-id="cc746-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="cc746-105">El elemento **EapHostUserCredentials** contiene el elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) , [**las credenciales**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) o el elemento [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cc746-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="cc746-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc746-106">Child elements</span></span>



| <span data-ttu-id="cc746-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc746-107">Element</span></span>                                                                                                | <span data-ttu-id="cc746-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc746-108">Type</span></span>                                                                                                                | <span data-ttu-id="cc746-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc746-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc746-110">**Credenciales**</span><span class="sxs-lookup"><span data-stu-id="cc746-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="cc746-111">**BaseEapMethodUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="cc746-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="cc746-112">Se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="cc746-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="cc746-113">**CredentialsBlob**</span><span class="sxs-lookup"><span data-stu-id="cc746-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="cc746-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="cc746-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="cc746-115">Se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.</span><span class="sxs-lookup"><span data-stu-id="cc746-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="cc746-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="cc746-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="cc746-117">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="cc746-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="cc746-118">Identifica el método al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="cc746-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="cc746-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc746-119">Remarks</span></span>

<span data-ttu-id="cc746-120">Las [**credenciales**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) y los elementos [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="cc746-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="cc746-121">Hay un punto de extensión para otros espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="cc746-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="cc746-122">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="cc746-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="cc746-123">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="cc746-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc746-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc746-124">Requirements</span></span>



| <span data-ttu-id="cc746-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc746-125">Requirement</span></span> | <span data-ttu-id="cc746-126">Value</span><span class="sxs-lookup"><span data-stu-id="cc746-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc746-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc746-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc746-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc746-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc746-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc746-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc746-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc746-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc746-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc746-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc746-132">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="cc746-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cc746-133">Esquema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="cc746-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





